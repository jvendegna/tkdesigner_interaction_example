# TK_Designer_Demo

The purpose is to show a simple page transition using output from tkdesigner

## [Figma File](https://www.figma.com/file/LeDp52QSe7qM8VQLTT5nRD/tkd2PageExample?node-id=1%3A11)



# Instructions

1. `python build/gui.py`
2. Click both buttons.
3. Note that in gui.py there is a section of code for buttons which creates a command for that button/element.
4. Change the highlighted area to do your bidding

![shows where the command lambda line is in gui.py Button objects](https://raw.githubusercontent.com/jvendegna/tkdesigner_interaction_example/main/images/capture.PNG)



# Examples


__Create a button with a button__


```
def create_new_button(x_coord, y_coord):
    button_image_3 = PhotoImage(file=relative_to_assets("button_1.png"))

    button_3 = Button(
        image=button_image_3,
        borderwidth=0,
        highlightthickness=0,
        command=lambda: print("button_1 clicked"),
        relief="flat",
    )
    button_3.place(x=x_coord, y=y_coord, width=120.0, height=37.0)


button_image_1 = PhotoImage(file=relative_to_assets("button_1.png"))
button_1 = Button(
    image=button_image_1,
    borderwidth=0,
    highlightthickness=0,
    command=lambda: create_new_button(65, 65),
    relief="flat",
)
button_1.place(x=371.0, y=216.0, width=120.0, height=37.0)
```

# Contributing

Open an issue with something you'd like to see and I'll try to work it out or provide examples yourself. Just be chill and have fun.