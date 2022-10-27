name : Levenshtein distance/alignment
tags : 
backlinks : 
source : https://en.wikipedia.org/wiki/Levenshtein_distance

###### Content:
The Levenshtein distance is a string metric for measuring the difference between two sequences. Informally, the Levenshtein distance between two words is the minimum number of single-character edits (insertions, deletions, or substitutions) required to change one word into the other.

|     |     | k   | i   | t   | t   | e   | n   |
| --- | --- | --- | --- | --- | --- | --- | --- |
|     | **0**   | 1   | 2   | 3   | 4   | 5   | 6   |
| s   | 1   | **1**   | 2   | 3   | 4   | 5   | 6   |
| i   | 2   | 2   | **1**   | 2   | 3   | 4   | 5   |
| t   | 3   | 3   | 2   | **1**   | 2   | 3   | 4   |
| t   | 4   | 4   | 3   | 2   | **1**   | 2   | 3   |
| i   | 5   | 5   | 4   | 3   | 2   | **2**   | 3   |
| n   | 6   | 6   | 5   | 4   | 3   | 3   | **2**   |
| g   | 7   | 7   | 6   | 5   | 4   | 4   | **3**    |


*Note: This method can also be used to align numeric sequences by making the substitution cost dependent on the differences between the scalar values.*

```matlab
	% Isolate columns of interest so I don't have to keep typing out
    % (:,col*)
    va = mat_1(:,col_1);
    vb = mat_2(:,col_2);
    
    % Create matrix for alignment values for levenshtein distance
    lev = zeros(length(va),length(vb));
    lev(1,1) = 0;

    for i = 2:length(va)
        lev(i,1) = i-1;
    end
    for j = 2:length(vb)
        lev(1,j) = j-1;
    end

    % Go through the combinations of values and calculate the
    % substitution costs between values
    for j = 2:length(vb)
	for j = 2:length(vb)
		for i = 2:length(va)
			if va(i) == vb(j)
				substitutionCost = 0;
			else
				substitutionCost = abs(va(i) - vb(j))/subcost;
			end
			lev(i,j) = min([lev(i-1,j)+1, lev(i,j-1)+1, lev(i-1, j-1)+substitutionCost]);
		end
	end


    [Y,I] = min(lev(end,:));

    [r,c] = size(lev);
    c = I;

    % Create the vector move which will store the movements that the
    % computer follows along the lev matrix
    move = [];
    q_c = 0;
    q_r = 0;

    while r > 0
        if c>1 && r>1
            q = min([lev(r,c-1),lev(r-1,c-1), lev(r-1,c)]);
        elseif r == 1 && c~=1
            q = lev(r,c-1);
            q_r = 1;
        elseif c == 1 && r ~=1
            q = lev(r-1,c);
            q_c = 1;
        end

        if r == 1
            move(end+1:end+c-1) = 1;
            r= 0;
        elseif c == 1
            move(end+1:end+r-1) = 2;
            r = 0;
        elseif q == lev(r-1,c-1)
            move=[move,0]; %diag
            r=r-1;
            c=c-1;
        elseif q == lev(r,c-1) && q_c ~=1
            move=[move,1]; %left
            c=c-1;
        elseif q == lev(r-1,c) && q_r ~=1
            move=[move,2]; %up
            r = r-1;
        elseif q_c == 1 && q_r == 1
            r=r-1;
            c=c-1;
        end

    end
    move = [move,0];

    % Flip move for path to maximize alignment
    move = flip(move,2);

    % Clean up a bunch of variables that were made during this process
    clear i j c r I line pks_a q q_c q_r Y substitutionCost;

    % Realign the two matrices 
    j = 1;
    aligned=[];
    
    for i = 1:length(move)
        if move(1,i) == 0
            aligned(end+1,:) = mat_2(j,:);
            j = j+1;
        elseif move(1,i) == 1
            j = j+1;
        elseif move(1,i) == 2
            aligned(end+1,:) = NaN;
        end
    end
end
```

###### Properties:
- This was used in the alignment of RR-intervals and RR-intervals generated from the [[electrocardiogram (ECG)]] data by creating a Levenshtein distance matrix and using the results to determine where to insert or delete RR-interval values generated from the ECG data: https://github.com/Lawreros/PSHR_pipeline/blob/main/Preprocess/levenshtein_align.m

###### Additional Thoughts:
