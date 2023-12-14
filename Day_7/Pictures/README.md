# Day 7: [Log analysis] ‘Tis the season for log chopping!
Additional walktrough [video](https://www.youtube.com/watch?v=cG8UH8xwmaY)


## Steps

1. Read the story about **Tracy McGreedy** incase its contain clue to solving the problem

2. Familiarise with linux command to view file/log, instruction in the room for Day 7 task
   * cat, less, head, tail, wc, nl 

3. Press the "Start Machine" button to initiate the AttackBox
    * ![AttackBox](Pictures/1.png)

4. Solve following questions
    * ![tasks](Pictures/2.png)

5. Enumerate all directories and files are available in the disk
    * ![directory](Pictures/3.png)
    * ![File/Folder](Pictures/9.png)
    * ![File/Folder](Pictures/10.png)
    * ![File/Folder](Pictures/5.png)
    * ![File/Folder](Pictures/6.png)
    * ![File/Folder](Pictures/7.png)
    * ![File/Folder](Pictures/8.png)

6. Identify the file size (byte) for ```AC2023.BAK```
    * ![AC2023.BAK size](Pictures/4.png)

7. Navigate to TOOLS\BACKUP folder to use the backup program
    * ![busmaster backup program](Pictures/11.png)

8. Run ```BUMASTER.EXE C:\AC2023.BAK``` to inspect the backup file
    * Encountered error, need to refer ```readme.txt``` file
    * ![busmaster backup program](Pictures/12.png)
    * ![backup readme](Pictures/13.png)

9.  From ```readme.txt``` file, the file's signatures  should begin with ```41 43``` which is ```AC``` in ASCII
    * ![Hexa to ASCII](Pictures/14.png)
    * Obtained name of backup program as well
        * ![Program name](Pictures/18.png)

10. ```AC2023.BAK``` begun with ```XX``` ASCII code (```58 58``` in Hex). The file is corrupted (or incompatible)
    * ![AC2023 File signatures](Pictures/15.png)

11. Edit the file with correct file signatures, and save the file 
    * ![Correct AC2023 File signatures](Pictures/16.png)

12. Run ```BUMASTER.EXE C:\AC2023.BAK``` again to restore backup
    * Flag obtained, ```THM{0LD_5CH00L_C00L_d00D}```
    * ![Flag](Pictures/17.png)

13. Submit all answers obtained 
    * ![Submit answer](Pictures/19.png)