from tkinter import *
root= Tk()
import pymysql

TURN=1
remain=21
counter=0
def login():
    master=Toplevel()
    username=t1.get()
    password=t2.get()
    db=pymysql.connect(host='localhost',user='root',password='kriti@123',db=game)
    sql="select*from login where username=%s and password=%s"
    val=(username,password)
    cur=db.cursor()
    cur.execute(sql,val)
    for row in cur.fetchall():
        uname=row[1]
        upassword=row[2]
    def show():
        global TURN
        global remain
        global counter
        c = int(coin.get())
        # print(c)
        if(TURN%2!=0 and remain>=17):

            if(c==1):
                b21.config(text="*")
                turn.config(text="AI Turn")
                TURN=TURN+1
                remain=remain-1
                counter=1
                c=0


            elif(c==2):
                b21.config(text="*")
                b20.config(text="*")
                turn.config(text="AI Turn")
                TURN = TURN + 1
                remain = remain - 2
                counter = 2
                c = 0
            elif (c == 3):
                b21.config(text="*")
                b20.config(text="*")
                b19.config(text="*")
                turn.config(text="AI Turn")
                TURN = TURN + 1
                remain = remain - 3
                counter = 3
                c=0

            elif (c == 4):
                b21.config(text="*")
                b20.config(text="*")
                b19.config(text="*")
                b18.config(text="*")
                turn.config(text="AI Turn")
                TURN = TURN + 1
                remain = remain - 4
                counter = 4
                c = 0
        else:
            if(remain>4):
                if(c==1):
                    b20.config(text="*")
                    b19.config(text="*")
                    b18.config(text="*")
                    b17.config(text="*")
                    turn.config(text="Your Turn")
                    TURN = TURN + 1
                    remain = remain - 4
                    counter = 5
                    c=0
                elif(c==2):

                    b19.config(text="*")
                    b18.config(text="*")
                    b17.config(text="*")
                    b16.config(text="*")
                    turn.config(text="Your Turn")
                    TURN = TURN + 1
                    remain = remain - 4
                    counter=6
                    c=0

                elif (c ==3):
                    b18.config(text="*")
                    b17.config(text="*")
                    b16.config(text="*")
                    b15.config(text="*")
                    turn.config(text="Your Turn")
                    TURN = TURN + 1
                    remain = remain - 4
                    counter = 7
                    c=0

                elif (c ==4):
                    b17.config(text="*")
                    b16.config(text="*")
                    b15.config(text="*")
                    b14.config(text="*")
                    turn.config(text="Your Turn")
                    TURN = TURN + 1
                    remain = remain - 4
                    counter = 8
                    c=0


        if (TURN % 2 != 0 and remain >= 10):

            if(c==1):
                b13.config(text="*")
                turn.config(text="AI Turn")
                TURN = TURN + 1
                remain = remain - 1
                counter = 9

            elif (c ==2):
                b13.config(text="*")
                b12.config(text="*")
                turn.config(text="AI Turn")
                TURN = TURN + 1
                remain = remain - 2
                counter = 11
            elif (c == 3):
                b13.config(text="*")
                b12.config(text="*")
                b11.config(text="*")
                turn.config(text="AI Turn")
                TURN = TURN + 1
                remain = remain - 3
                counter = 13
            elif (c == 4):
                b13.config(text="*")
                b12.config(text="*")
                b11.config(text="*")
                b10.config(text="*")
                turn.config(text="AI Turn")
                TURN = TURN + 1
                remain = remain - 4
                counter = 14
        else:
            if (remain > 4):
                if (c == 1):
                    b9.config(text="*")
                    b8.config(text="*")
                    b7.config(text="*")
                    b6.config(text="*")
                    turn.config(text="Your Turn")
                    TURN = TURN + 1
                    remain = remain - 4
                    counter = 13
                elif (c == 2):

                    b8.config(text="*")
                    b7.config(text="*")
                    b6.config(text="*")
                    b5.config(text="*")
                    turn.config(text="Your Turn")
                    TURN = TURN + 1
                    remain = remain - 4
                    counter = 14
                elif (c == 3):
                    b7.config(text="*")
                    b6.config(text="*")
                    b5.config(text="*")
                    b4.config(text="*")
                    turn.config(text="Your Turn")
                    TURN = TURN + 1
                    remain = remain - 4
                    counter = 15
                elif (c == 4):
                    b6.config(text="*")
                    b5.config(text="*")
                    b4.config(text="*")
                    b3.config(text="*")
                    turn.config(text="Your Turn")
                    TURN = TURN + 1
                    remain = remain - 4
                    counter = 16

        if (TURN % 2 != 0 and remain <= 9):

            if(c == 1):
                b1.config(text="*")
                turn.config(text="AI Turn")
                TURN = TURN + 1
                remain = remain - 1
                counter = 8

            elif (c == 2):
                b1.config(text="*")
                b2.config(text="*")
                turn.config(text="AI Turn")
                TURN = TURN + 1
                remain = remain - 2
                counter = 7
            elif (c == 3):
                b1.config(text="*")
                b2.config(text="*")
                b3.config(text="*")
                turn.config(text="AI Turn")
                TURN = TURN + 1
                remain = remain - 3
                counter = 6
            elif (c == 4):
                b1.config(text="*")
                b2.config(text="*")
                b3.config(text="*")
                b4.config(text="*")
                turn.config(text="AI Turn")
                TURN = TURN + 1
                remain = remain - 4
                counter = 5
        else:
            if (remain > 4):
                if (c == 1):
                    b20.config(text="*")
                    b19.config(text="*")
                    b18.config(text="*")
                    b17.config(text="*")
                    turn.config(text="Your Turn")
                    TURN = TURN + 1
                    remain = remain - 4
                    counter = 4
                elif (c == 2):

                    b19.config(text="*")
                    b18.config(text="*")
                    b17.config(text="*")
                    b16.config(text="*")
                    turn.config(text="Your Turn")
                    TURN = TURN + 1
                    remain = remain - 4
                    counter = 3
                elif (c == 3):
                    b18.config(text="*")
                    b17.config(text="*")
                    b16.config(text="*")
                    b15.config(text="*")
                    turn.config(text="Your Turn")
                    TURN = TURN + 1
                    remain = remain - 4
                    counter = 2
                elif (c == 4):
                    b17.config(text="*")
                    b16.config(text="*")
                    b15.config(text="*")
                    b14.config(text="*")
                    turn.config(text="Your Turn")
                    TURN = TURN + 1
                    remain = remain - 4
                    counter = 1

                if(turn.config="Your Turn" and counter=1):
                    result.config(text="AI win")
                    INSERT INTO `login`(`id`, `username`, `password`, `attempt`, `scored`);
                    VALUES(NULL, 'admin', 'admin1234', '1', '1');

                else:
                    result.config(text="you win")
                    INSERT
                    INTO
                    `login`(`id`, `username`, `passworw`, `attempt`, `scored`)
                    VALUES(NULL, 'guest', 'guest1234', '1', '1');





    username=t1.get()
    password=t2.get()
    if username=="guest" and password=="guest1234" or username==uname and password==upassword :
        b1 = Button(master,text="", )
        b2 = Button(master,text="",)
        b3 = Button(master,text="", )
        b4 = Button(master,text="",)
        b5 = Button(master,text="", )
        b6 = Button(master,text="")
        b7 = Button(master,text="",)
        b8 = Button(master,text="", )
        b9 = Button(master,text="", )
        b10 = Button(master,text="", )
        b11 = Button(master,text="",)
        b12 = Button(master,text="", )
        b13 = Button(master,text="", )
        b14 = Button(master,text="",)
        b15 = Button(master,text="", )
        b16 = Button(master,text="",)
        b17 = Button(master,text="", )
        b18 = Button(master,text="", )
        b19 = Button(master,text="", )
        b20 = Button(master,text="", )
        b21 = Button(master,text="", )
        turn=Label(master,text="your turn")
        pick=Label(master,text="pick no. of coins(1 to 4):")
        coin=Entry(master)
        bs=Button(master,text="ok", command=show)
        result=Label(master,text="")
        b1.pack()
        b2.pack()
        b3.pack()
        b4.pack()
        b5.pack()
        b6.pack()
        b7.pack()
        b8.pack()
        b9.pack()
        b10.pack()
        b11.pack()
        b12.pack()
        b13.pack()
        b14.pack()
        b15.pack()
        b16.pack()
        b17.pack()
        b18.pack()
        b19.pack()
        b20.pack()
        b21.pack()
        turn.pack()
        pick.pack()
        coin.pack()
        bs.pack()
        result.pack()




l1=Label(text="username:")
t1=Entry()
l2=Label(text="password:")
t2=Entry()
b1=Button(text="login", command=login)
l1.pack()
t1.pack()
l2.pack()

t2.pack()
b1.pack()
mainloop()
