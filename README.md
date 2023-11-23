from tkinter import *
from tkinter import ttk

#2
class Admin :
    def __init__(self,main) :
        self.main = main
        self.T_Frame = Frame(self.main, height=50, width=1500, background='#dfe3ee',bd=2,relief=GROOVE)
        self.T_Frame.pack()
        self.Title = Label(self.T_Frame, text='ADD/REMOVE/UPDATE STUDENT', font='Arial 30 bold', width=1500, bg='#dfe3ee',fg='#000000')
        self.Title.pack()
        
        #3
        self.Frame_1 = Frame(self.main, height=800,  width=400, bd=2, relief=GROOVE,bg='#ffffff')  #bd=border, 2 pixels
        self.Frame_1.pack(side='left') 
        self.Frame_1.pack_propagate(0)
        
        #5
        Label(self.Frame_1, text='Student Details',background='#ffffff', font='arial 20 bold').place(x=20,y=30)
        
        self.name = Label(self.Frame_1, text = 'Student Name:', background = '#ffffff', font='arial 14 bold')
        self.name.place(x=20 ,y=100)
        self.name_Entry = Entry(self.Frame_1, width=18, font='arial 16 bold',background='#dfe3ee') 
        self.name_Entry.place(x=170, y=100) 
        
        #7
        self.id = Label(self.Frame_1, text = 'Student ID:', background = '#ffffff', font='arial 14 bold')
        self.id.place(x=20 ,y=150)
        self.id_Entry = Entry(self.Frame_1, width=18, font='arial 16 bold',background='#dfe3ee')  
        self.id_Entry.place(x=170, y=150)
        
        #8
        self.password = Label(self.Frame_1, text = 'Password:', background = '#ffffff', font='arial 14 bold')
        self.password.place(x=20 ,y=200)
        self.password_Entry = Entry(self.Frame_1, width=18, font='arial 16 bold',background='#dfe3ee') 
        self.password_Entry.place(x=170, y=200)
        
        #9
        self.email = Label(self.Frame_1, text = 'Student Email:', background = '#ffffff', font='arial 14 bold')
        self.email.place(x=20 ,y=250)
        self.email_Entry = Entry(self.Frame_1, width=18, font='arial 16 bold',background='#dfe3ee')
        self.email_Entry.place(x=170, y=250) 
        
        #10
        self.faculty = Label(self.Frame_1, text = 'Faculty:', background = '#ffffff', font='arial 14 bold')
        self.faculty.place(x=20 ,y=300)
        self.faculty_Entry = Entry(self.Frame_1, width=18, font='arial 16 bold',background='#dfe3ee')
        self.faculty_Entry.place(x=170, y=300)
        
        #11
        self.programme = Label(self.Frame_1, text = 'Programme:', background = '#ffffff', font='arial 14 bold')
        self.programme.place(x=20 ,y=350)
        self.programme_Entry = Entry(self.Frame_1, width=18, font='arial 16 bold',background='#dfe3ee') 
        self.programme_Entry.place(x=170, y=350)
        
        #12
        self.contactnumber = Label(self.Frame_1, text = 'Contact.Num:', background = '#ffffff', font='arial 14 bold')
        self.contactnumber.place(x=20 ,y=400)
        self.contactnumber_Entry = Entry(self.Frame_1, width=18, font='arial 16 bold',background='#dfe3ee') 
        self.contactnumber_Entry.place(x=170, y=400)
        
        self.gender = Label(self.Frame_1, text = 'Gender:', background = '#ffffff', font='arial 14 bold')
        self.gender.place(x=20 ,y=450)
        self.gender_Entry = Entry(self.Frame_1, width=18, font='arial 16 bold',background='#dfe3ee') 
        self.gender_Entry.place(x=170, y=450)
        
        self.Button_Frame = Frame(self.Frame_1, height=150, width=200, relief=GROOVE,bd=2, bg='#dfe3ee')
        self.Button_Frame.place(x=80,y=525)
  
        self.Add = Button(self.Button_Frame, text='Add',width=25,font='arial 11 bold',command=self.Add)
        self.Add.pack()
        self.Remove = Button(self.Button_Frame, text='Remove',width=25,font='arial 11 bold',command=self.Remove)
        self.Remove.pack()
        self.update = Button(self.Button_Frame, text='Update',width=25,font='arial 11 bold',command=self.update)
        self.update.pack()
        self.clear = Button(self.Button_Frame, text='Clear',width=25,font='arial 11 bold',command=self.clear)
        self.clear.pack()
 
        self.Frame_2 = Frame(self.main,height=800,width=1100, bd=2, relief=GROOVE,bg='#dfe3ee')
        self.Frame_2.pack(side=RIGHT)
        
        self.tree = ttk.Treeview(self.Frame_2,columns =('c1','c2','c3','c4','c5','c6', 'c7','c8'),show='headings',height=30)
        self.tree.pack()

        #17
        self.tree.column('#1', anchor=CENTER,width=140)
        self.tree.heading('#1',text='Student Name')
        
        self.tree.column('#2', anchor=CENTER,width=130)
        self.tree.heading('#2',text='Student ID')
        
        self.tree.column('#3', anchor=CENTER,width=150)
        self.tree.heading('#3',text='Password')
        
        self.tree.column('#4', anchor=CENTER,width=200)
        self.tree.heading('#4',text='Student Email')
        
        self.tree.column('#5', anchor=CENTER,width=95)
        self.tree.heading('#5',text='Faculty')
        
        self.tree.column('#6', anchor=CENTER,width=115)
        self.tree.heading('#6',text='Programme')
        
        self.tree.column('#7', anchor=CENTER,width=140)
        self.tree.heading('#7',text='Contact Number')
        
        self.tree.column('#8', anchor=CENTER,width=120)
        self.tree.heading('#8',text='Gender')

        self.tree.insert('',index=0,values=('thisisSTUDENT1','StudentID','ssttuuddeenntt11','studentid@student.mmu.edu.my','FCI','Foundation in IT','012-345-6789','Female'))
        self.tree.insert('',index=0,values=('thisisSTUDENT2','StudentID','ssttuuddeenntt22','studentid@student.mmu.edu.my','FCI','Foundation in IT','012-345-6789','Female'))
        self.tree.insert('',index=0,values=('thisisSTUDENT3','StudentID','ssttuuddeenntt33','studentid@student.mmu.edu.my','FCI','Foundation in IT','012-345-6789','Female'))
        self.tree.insert('',index=0,values=('thisisSTUDENT4','StudentID','ssttuuddeenntt44','studentid@student.mmu.edu.my','FCI','Foundation in IT','012-345-6789','Female'))
        self.tree.insert('',index=0,values=('thisisSTUDENT5','StudentID','ssttuuddeenntt55','studentid@student.mmu.edu.my','FCI','Foundation in IT','012-345-6789','Female'))
        self.tree.insert('',index=0,values=('thisisSTUDENT6','StudentID','ssttuuddeenntt66','studentid@student.mmu.edu.my','FCI','Foundation in IT','012-345-6789','Female'))
        self.tree.insert('',index=0,values=('thisisSTUDENT7','StudentID','ssttuuddeenntt77','studentid@student.mmu.edu.my','FCI','Foundation in IT','012-345-6789','Female'))
        self.tree.insert('',index=0,values=('thisisSTUDENT8','StudentID','ssttuuddeenntt88','studentid@student.mmu.edu.my','FCI','Foundation in IT','012-345-6789','Female'))
        self.tree.insert('',index=0,values=('thisisSTUDENT9','StudentID','ssttuuddeenntt99','studentid@student.mmu.edu.my','FCI','Foundation in IT','012-345-6789','Female'))
        self.tree.insert('',index=0,values=('thisisSTUDENT10','StudentID','ssttuuddeenntt1010','studentid@student.mmu.edu.my','FCI','Foundation in IT','012-345-6789','Female'))
        self.tree.pack()

    def Add(self):
        name = self.name_Entry.get()
        id = self.id_Entry.get()
        password = self.password_Entry.get()
        email = self.email_Entry.get()
        faculty = self.faculty_Entry.get()
        programme = self.programme_Entry.get()
        contactnumber = self.contactnumber_Entry.get()
        gender = self.gender_Entry.get()
        self.tree.insert('',index=0,values=(name,id,password,email,faculty,programme,contactnumber,gender))
          
    def Remove(self):
        item = self.tree.selection()[0]
        self.tree.delete(item) 
        
    def update(self): 
        name = self.name_Entry.get()
        id = self.id_Entry.get()
        password = self.password_Entry.get()
        email = self.email_Entry.get()
        faculty = self.faculty_Entry.get()
        programme = self.programme_Entry.get()
        contactnumber = self.contactnumber_Entry.get()
        gender = self.gender_Entry.get()
        item = self.tree.selection()[0]
        self.tree.item(item,values=(name,id,password,email,faculty,programme,contactnumber,gender) )
        
    def clear(self):  #clear everything all the left frame
        self.name_Entry.delete(0,END)
        self.id_Entry.delete(0,END)
        self.password_Entry.delete(0,END)
        self.email_Entry.delete(0,END)
        self.faculty_Entry.delete(0,END)
        self.programme_Entry.delete(0,END)
        self.contactnumber_Entry.delete(0,END)
        self.gender_Entry.delete(0,END)

#1
main = Tk()
main.title('Admin Management System')
main.resizable(False, False)
main.geometry('1500x800')

Admin(main)




main.mainloop()
