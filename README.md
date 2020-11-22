# COMP268

This page records codes for COMP268 assignments

Assignment1 Program 1 in Python

    for column in range(0, 13):
        for row in range(0, 13):
            if row == 0:
                if column == 0:
                    print("     ", end="|")
                else:
                    if column <=9:
                        print("  ", column, "", end="|")
                    else:
                        print(" ", column, "", end="|")

            elif column == 0:
                if row <= 9:
                    print("  ", row, "", end="|")
                else:
                    print(" ", row, "", end="|")
            else:
                result = row * column
                if result <= 9:
                    space = "  "
                elif result <= 99:
                    space = " "
                elif result <= 144:
                    space = ""
        
                print(space, result, "", end="|")
        print()

