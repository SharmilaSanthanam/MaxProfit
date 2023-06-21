MAX PROFIT PROBLEM:

Mr. X owns a large strip of land in Mars Land. For the purposes of this problem
assume that he has infinite land capacity. On each parcel of he can choose to
develop it as per his wishes. He can build either Theatres, Pubs or Commercial
Park. Commercial Park houses 6 Commercial Spaces and 8 Screen Theatres.
• A Theatre takes 5 units of time to build and covers 2x1 parcel of land.
• A Pub takes 4 units of time to develop and covers 1x1 parcel of land.
• A Commercial Park takes 10 units of time to build and covers 3x1 parcel
of land.
Each period of time that a building is operational it earns him money.

Establishment    Earning
Theatre           $1500
Pub               $1000
Commercial Park   $3000

He cannot have two properties being developed in parallel in one unit of time.
• After n units of time where n is the input, he earns money based on which
properties have been developed.
• The output should be T for Theatre followed by number developed, P for
Pub followed by number developed and C for Commercial Park followed
by number developed.

Challenge
• Come up with the right mix of properties based on the period of time
given as input.

Test Case 1
Time Unit: 7
Earnings: $3000
Solutions
1. T: 1 P: 0 C: 0
2. T: 0 P: 1 C: 0

Test Case 2
Time Unit: 8
Earnings: $4500
Solutions
1. T: 1 P: 0 C: 0

Test Case 3
Time Unit: 13
Earnings: $16500
Solutions
1. T: 2 P: 0 C: 0


Solution:

Starting from day 1, we calculate which of the three choices (i.e. theatre/pub/commercial park) will give the max earning at 'stage1' and update the cost and the choice. For example- On day one, for maximum earning we decide that Theatre is built first, then we deduct the 5 days (i.e. the time taken to build theatre) from total days to calculate the remaining days for the stage 2 and then again calcualte which is the most profitable choice to build for stage2, and deduct time for completing that choice to calculate remaining days and so on till the time when remaining days <=4 (i.e. the least time required to build something)

Possibility of earnings from two of the three options being same at any "stage":There are 3 possible combinations.
1 Theatre+Pub=7 days left - this will lead to multiple outputs as building theatre or pub is equally profitable
2 Pub+Commercial Park=13 days left - Here Theatre gives maximum value of earning so both Pub and commercial park are not outputs
3 Theatre+Commercial=15 units left - At this stage- both theatre and conference park will give same earning at that stage but choosing theatre at that stage will give more "overall profit" since there will be option to earn more in next stages- so Theatre option wins in case of a tie of earnings between theatre and commerical park at any stage