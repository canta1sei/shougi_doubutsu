# shougi_doubutsu
import tkinter as tk

class App(tk.Tk):
    def __init__(self):
        super(App,self).__init__()
        self.title("動物将棋")
        self.geometry('400x400')
        self.resizable(width=0,height=0)

    def set_widgets(self):#将棋盤を作る
        self.board = tk.Canvas(self,width=400,height=400,bg="Peach Puff3")
        self.board.pack()
        
        size=60
        tate=4
        yoko=3
        for i in range(tate):
            for j in range(yoko):
                self.board.create_rectangle((size+size*j,50+size*i
                　　　　　　　　　　　　　　　　　,+size+size*(j+1),50+size*(i+1))
                                 　　　　　　　,fill="white")
        
    def run(self):
        self.mainloop()


if __name__=="__main__":
    app=App()
    app.set_widgets()
    app.run()
