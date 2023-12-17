# Day 2 - [Log analysis] O Data, All Ye Faithful
Additional walktrough [video](https://www.youtube.com/watch?v=YbFqW2pjcrQ)


## Steps
1. Start machine for the task, wait for VM machince to appear in split view
   * ![VM](Pictures/1.png)

2. Login to Jupyter Notebooks with default password on screen
   * ![Jupyter Notebooks](Pictures/2.png)

3. Refer task's guide on how to use python with Jupyter Notebooks
   * or additionally you can open 
     * Python 3 Introduction in Jupyter, `1_IntroToPython -> Python3CrashCourse.ipynb`
     * Panda Library Introduction in Jupyter, `2_IntroToPandas ->; IntroToPandas.ipynb`
     * Matplotlib Library Introduction in Jupyter, `3_IntroToMatplotib -> IntroToMatplotlib.ipynb`
   * ![Python Course](Pictures/3.png)

4. Open `Workbook.ipynb` in `4_Capstone` directory
   * ![Packet](Pictures/4.png)

5. The stucture of packet information in cfv file, & required library to run the code.
   * ![CSV+Python](Pictures/5.png)

6. Insert a cell to run our code
   * ![Add Cell](Pictures/6.png)

7. Copy required codes, select the cell, and try to run the code
   * ![Add Code](Pictures/7.png)
   * ![Run Code](Pictures/8.png)
   * ![Run Code](Pictures/9.png)

8. Write a code to get total of **PacketNumber**
    ```python
    packet = df.count
    print(packet)
    ```
   * ![Total Packets](Pictures/10.png)
   * Or simply use `df.count()`
     * ![Total Packets](Pictures/11.png)
   * **100 Packets** in total 


9. Identify **IP address** with **most traffic (sent)** during packet capture
   * Use `df.groupby(['Source']).size()` code
   * ![Top IP](Pictures/12.png)
   * `10.10.1.4 `

10. Identify frequent **Protocol** on captured packets
    ```python
    df.groupby(['Protocol']).size().sort_values(ascending=False)  
    ```
   * ![Frequent Protocol](Pictures/13.png)

11. Submit all answers obtained 
    * ![Submit answer](Pictures/14.png)