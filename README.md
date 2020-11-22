# COMP268

This page records codes for COMP268 assignments

Assignment1 Program 1 in Python
#Just by looking at the table, a few things to notice
#There is a special cell, column0/row0 is an empty cell
#row0 and column0 are not results of multiplication, but rather headings

for column in range(0, 13):
#This is a loop between 0 and 12, not 13
    for row in range(0, 13):
    #This is a nested loop
        if row == 0:
            if column == 0:
                print("     ", end="|")
            #This print special cell row0/column0
            else:
                if column <=9:
                    print("  ", column, "", end="|")
                else:
                    print(" ", column, "", end="|")
            #This will print the first row(i.e.heading)
        elif column == 0:
            if row <= 9:
                print("  ", row, "", end="|")
            else:
                print(" ", row, "", end="|")
            #This will print the first column(i.e.heading)

        else:
            result = row * column
            if result <= 9:
                space = "  "
            elif result <= 99:
                space = " "
            elif result <= 144:
                space = ""
            # These 3 elif fix the issue of different spacing for numbers with different digits
            print(space, result, "", end="|")

    print()
    #this print is important!!
    #I think this print will print all results coming out of the nested loop
