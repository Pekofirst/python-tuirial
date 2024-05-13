# python-tuition
'''I am new here and try to be skillful in python.Next, I will take down the details during my study period.  
hope to be a better time  
May 5:  
I summarize my ability:  
I'm from China which is a fierce-competed country and My original major is accounting.I have middle-level skills on python, accounting and english.  
what i want to do next:  
1.python's code design logic:i am not good at the logic of any application.i didnot acquire the systemic education about the code's world.  
2.english learning:maybe it is enough to handle every english test in China,i can not accept only live domestic.If it is possible, i prefer to be in Hong-Kong   
3.Frence learning:i take language like a tool. Actually, it is.  
hope to be a better one.'''  
May 7:  
i am here to declare i do not want to be a nitte anymore.i am fed up with fearing the changingable world, Internet has got me mad for everything i saw is booming.  
After played the epic game 'edith finch's memory'(maybe it is not its real name),i really decided to write down my feelings about everydays' life.  
i will take this place as a journal to set my goal and try to reach it.  
You know,it is hard to keep our innovate heart in the chaos.what i see everyday is barely junks who is playing the junk game allday.  
I can be sure i know why they done like this,they are same as me.I have live for a invisible score before,i lose my destination at college.  
i want to see my daily-life can be changed since i have been dizzy during past 2 years.  
hope this dairy will keep an eye on what i am doing everyday so i won't be so down after the next 2 years.  
sincerely,yours  
May 13:  
![QY@FU6TM9_Z7)WWM6SG$_OO](https://github.com/Pekofirst/python-tuirial/assets/168003043/452a3bbd-9f14-469a-96f8-8c7567e93eb3)
i will back to the normal pace now.i won't let everything down me over 2 days and i hope i can do it.  
now i want to tackle some realistic problem,i always in low-passion.i wanna make a PERSONNAL-MANAGER to monitor my study.  
i have scheduled its functions:it can take down the time i study and add them up to a container?  
when i wanna play games or relax,it can count down the 'time container' to make sure i would not paly too much.
i have got a timer and the 'note-down' function.but i still misunderstand how to solve the count-down function.
i would try other ways.
````python
from time import sleep
class clock:
    def __init__(self,hour=0,minute=0,second=0,swith=True):
        self.second=second
        self.hour=hour
        self.minute=minute
        self.swich=swith
    def _run(self):
        self.second+=1
        if self.second==60:
            self.second=0
            self.minute+=1
            if self.minute==60:
                self.minute=0
                self.hour+=1

    def _stop(self):
        self.swich=not self.swich
    def _show(self):
        return '%02d:%02d:%02d' % \
               (self.hour, self.minute, self.second)
def main():
    a = clock(23, 59, 58)
    while True:
        print(a._show())
        sleep(1)
        a._run()

from openpyxl import Workbook,load_workbook
wb=load_workbook('timebook.xlsx')
ws=wb.active
def writetoexcel(x):
    ws.append(x)
    wb.save('timebook')
def loadresidualtime():
    residual_time=0
    for cell in ws['B']:
        cell_value=cell.value
        if cell_value is not None:
             residual_time+=cell_value

    return residual_time
from tkinter import *
root=Tk()
project=[]
screen=Listbox(root)

def insert(x):
    for i in x:
        screen.insert("end",i)
def startorstop():
    if Button["text"]==True:
        Button.config=not Button.config
        timer=clock()
````
oops!and i have not find a perfect gui yet.Maybe i can consider the vue3?

