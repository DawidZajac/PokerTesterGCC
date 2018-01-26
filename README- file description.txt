simulationFiles/config/backup.txt: Is used to store the players winnings, in case the simulation crashes before finishing, 
frequency of saving is chosen within the configuration file.
---------
simulationFiles/config/config.txt: configuration the casino uses, loaded before the simulation starts. All fields must be 
filled in the presented way, else proper running of the simulation cannot be guaranteed.
The fields are:

playAreaPathEven the path, with the name, of the read-only file to be created/edited - used on even numbered iterations. 
The format is as follows: C:\\Users\\...\\playAreaEven.txt

playAreaPathOdd the path, with the name, of the read-only file to be created/edited - used on odd numbered iterations. 
The format is as follows: C:\\Users\\...\\playAreaOdd.txt

userPath- the path to the directory where the players will write their decisions and receive their cards. 
The format is as follows: C:/Users/.../bots

maxRaises- the maximum number of raises in a betting round. 4 is recommended.

ante- a stake put up by a player in poker before receiving cards. 1 is recommended.

smallBlind- the minimum bet, used in the first 2 betting rounds. 4 is recommended.

bigBlind- the maximum bet, used in the last 2 betting rounds. Double the small blind. 8 is recommended.

players- the amount of players playing. Any number above 2 is recommended. 
Note that if there are more players than the number specifies, they will be ignored.

time_- time given to each player to make a decision. It scales with the current betting round, and as such, 
it starts at 1/4 of the given value and scales evenly across all 4 betting rounds, up to the full duration

monteCarloLength- number of iterations of the simulation. It is recommended to take the time constraint given 
above as a guide to what this should be, as to not have to wait too long

backupScores- how often should the player scores be backed up, in case of a crash. 
Recommended is 5, or any reasonable number that divides into the monteCarloLength.

backupPath- the path to the backupPath, recommended to be in the same directory as the configuration file. 
The format is as follows: C:/Users/.../config/backup.txt
