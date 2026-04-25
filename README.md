# UNWSP-Python-Week-12
import tkinter
import tkinter.messagebox

class GasGUI:
    def __init__(self):
        self.main_window = tkinter.Tk()
        self.main_window.title('MPG Calculator')
        self.gallons_frame = tkinter.Frame(self.main_window)
        self.miles_frame = tkinter.Frame(self.main_window)
        self.button_frame = tkinter.Frame(self.main_window)
        self.gallons_label = tkinter.Label(self.gallons_frame, text='Enter gallons of gas:')
        self.gallons_entry = tkinter.Entry(self.gallons_frame, width=10)
        self.gallons_label.pack(side='left')
        self.gallons_entry.pack(side='left')
        self.miles_label = tkinter.Label(self.miles_frame, text='Enter miles driven on a on full tank:')
        self.miles_entry = tkinter.Entry(self.miles_frame, width=10)
        self.miles_label.pack(side='left')
        self.miles_entry.pack(side='left')
        self.calc_button = tkinter.Button(self.button_frame, text='Calculate MPG', command=self.calculate)
        self.quit_button = tkinter.Button(self.button_frame, text='Quit', command=self.main_window.destroy)
        self.calc_button.pack(side='left')
        self.quit_button.pack(side='left')
        self.gallons_frame.pack()
        self.miles_frame.pack()
        self.button_frame.pack()
        tkinter.mainloop()
    def calculate(self):

            gallons = float(self.gallons_entry.get())
            miles = float(self.miles_entry.get())
            mpg = miles / gallons

            tkinter.messagebox.showinfo('Results', f'Miles Per Gallon = {mpg}')


if __name__ == '__main__':
    mpg_calc = GasGUI()


    import tkinter
import tkinter.messagebox
class Joes_Automotive_GUI:
        def __init__(self):
            self.main_window = tkinter.Tk()
            self.main_window.title('Joes Automotive GUI')
            self.top_frame = tkinter.Frame(self.main_window)
            self.bottom_frame = tkinter.Frame(self.main_window)
            self.oil_var = tkinter.IntVar()
            self.lube_var = tkinter.IntVar()
            self.rad_var = tkinter.IntVar()
            self.trans_var = tkinter.IntVar()
            self.insp_var = tkinter.IntVar()
            self.muff_var = tkinter.IntVar()
            self.tire_var = tkinter.IntVar()
            self.cb1 = tkinter.Checkbutton(self.top_frame, text='Oil Change', variable=self.oil_var)
            self.cb2 = tkinter.Checkbutton(self.top_frame, text='Lube Job', variable=self.lube_var)
            self.cb3 = tkinter.Checkbutton(self.top_frame, text='Radiator Flush', variable=self.rad_var)
            self.cb4 = tkinter.Checkbutton(self.top_frame, text='Transmission Fluid', variable=self.trans_var)
            self.cb5 = tkinter.Checkbutton(self.top_frame, text='Inspection', variable=self.insp_var)
            self.cb6 = tkinter.Checkbutton(self.top_frame, text='Muffler Replacement',variable=self.muff_var)
            self.cb7 = tkinter.Checkbutton(self.top_frame, text='Tire Rotation', variable=self.tire_var)
            self.cb1.pack()
            self.cb2.pack()
            self.cb3.pack()
            self.cb4.pack()
            self.cb5.pack()
            self.cb6.pack()
            self.cb7.pack()
            self.top_frame.pack()
            self.bottom_frame.pack()
            self.calc_button = tkinter.Button(self.bottom_frame, text='Calculate Total', command=self.calculate)
            self.quit_button = tkinter.Button(self.bottom_frame, text='Quit', command=self.main_window.destroy)
            self.calc_button.pack(side='left')
            self.quit_button.pack(side='left')
            tkinter.mainloop()
        def calculate(self):
            total = 0.0
            if self.oil_var.get() ==1: total += 30
            if self.lube_var.get() ==1: total += 20
            if self.rad_var.get() ==1: total += 40
            if self.trans_var.get() ==1: total += 100
            if self.insp_var.get() ==1: total += 35
            if self.muff_var.get() ==1: total += 200
            if self.tire_var.get() ==1: total += 20
            tkinter.messagebox.showinfo('Total Charges', f'Your total charges are: {total}')
if __name__ == '__main__':
    Automotive_Gui = Joes_Automotive_GUI()



import tkinter
import tkinter.messagebox


class LongDistanceCallsGUI:
    def __init__(self):
        self.main_window = tkinter.Tk()
        self.main_window.title('Long-Distance Calls')
        self.top_frame = tkinter.Frame(self.main_window)
        self.mid_frame = tkinter.Frame(self.main_window)
        self.bottom_frame = tkinter.Frame(self.main_window)
        self.radio_var = tkinter.IntVar()
        self.radio_var.set(1)
        self.rb1 = tkinter.Radiobutton(self.top_frame, text='Daytime (6:00 A.M. through 5:59 P.M.)',variable=self.radio_var, value=1)
        self.rb2 = tkinter.Radiobutton(self.top_frame, text='Evening (6:00 P.M.through 11:59 P.M.)',variable=self.radio_var, value=2)
        self.rb3 = tkinter.Radiobutton(self.top_frame, text='Off-Peak (Midnight through 5:59 A.M.)',variable=self.radio_var, value=3)
        self.rb1.pack()
        self.rb2.pack()
        self.rb3.pack()
        self.prompt_label = tkinter.Label(self.mid_frame, text='Enter minutes:')
        self.minutes_entry = tkinter.Entry(self.mid_frame, width=10)
        self.prompt_label.pack(side='left')
        self.minutes_entry.pack(side='left')
        self.calc_button = tkinter.Button(self.bottom_frame, text='Calculate Charge', command=self.calculate)
        self.quit_button = tkinter.Button(self.bottom_frame, text='Quit', command=self.main_window.destroy)
        self.calc_button.pack(side='left')
        self.quit_button.pack(side='left')
        self.top_frame.pack()
        self.mid_frame.pack()
        self.bottom_frame.pack()
        tkinter.mainloop()
    def calculate(self):
            minutes = float(self.minutes_entry.get())
            if self.radio_var.get() == 1:
                rate = 0.02
            elif self.radio_var.get() == 2:
                rate = 0.12
            else:
                rate = 0.05
            total = minutes * rate
            tkinter.messagebox.showinfo('Total Charge', f'Total Charge: {total}')


if __name__ == '__main__':
    Call_Gui = LongDistanceCallsGUI()
    
