# GUITranslator.py
from tkinter import *
#จากไลบรารีชื่อ tkinter, * คือให้ดึงความสามารถหลักมาทั้งหมด
from tkinter import ttk # ttk is theme of tk

#----Google Translate----
from googletrans import Translator
translator = Translator()


GUI = Tk() #สร้างหน้าต่างหลัก
GUI.geometry('800x400') #กว้าง x สูง
GUI.title('โปรแกรมแปลภาษา by JosephDeKing') #ชื่อโปรแกรม

#-----config-----
FONT = ('Angsana New',15)

#----Label----
L = ttk.Label(GUI,text='กรุณากรอกคำศัพท์ที่ต้องการแปล',font=FONT)
L.pack()

#-------Entry (ช่องกรอกข้อความ)--------
v_vocab = StringVar() #กล่องเก็บข้อความ
FONT = ('Angsana New',15)
E1 = ttk.Entry(GUI,textvariable = v_vocab,font=FONT,width=40)
E1.pack(pady=20)


#-------Button (ปุ่มแปล)--------
def Translate():
    vocab = v_vocab.get() #.get คือการสั่งให้แสดงผล
    meaning = translator.translate(vocab,dest='th')
    print( vocab + ' : ' + meaning.text)
    print(meaning.pronunciation)
    v_result.set(vocab + ' : ' + meaning.text)
    
B1 = ttk.Button(GUI,text='Translate',command=Translate) #สร้างปุ่มขึ้นมา
B1.pack(ipadx=20,ipady=10) #show ปุ่นมาวางจากบนลงล่าง

#----Label----
L = ttk.Label(GUI,text='คำแปล',font=FONT)
L.pack()

#-----Result-----
v_result = StringVar() #นี่คือกล่องสำหรับเก็บคำแปล
FONT2 = ('Angsana New',20)
R1 = ttk.Label(GUI,textvariable=v_result,font=FONT2, foreground='green')
R1.pack()





GUI.mainloop() #ทำให้โปรแกรมรันได้ตลอดเวลาจนกว่าจะปิด (ต้องอยู่บรรทัดสุดท้าย)
