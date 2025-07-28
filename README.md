# programs12c Collection

*Made by jacober-calc for the HP12c calculator*

## Note from the Author

While these programs may be shared on various archives and forums related to HP calculators, the most recent version will always be found on this Github page and nowhere else. Please direct any contributions by way of bug reporting or suggestions to the relevant locations within this repo. Thank you for being interested my HP12c program solutions project and helping to make the routines more useful for future users to come.

## Download and Install

You can find a .txt file containing the program listing for each program routine contained within this collection. Download the .txt file to get the file listing.

There is no way to tranfer files to the HP12c so the user will need to manually input the program listing line-by-line in the P/R mode of the calculator. Instructions for this can be found in the HP12c User Manual and solutions guide book. The .txt file provided in the download includes the normal listing as well as the calculator input (using the keyboard matrix). More information about these lines of display can be found in the User Manual.

## About this Collection

I will update this collect periodically as new programs are prepared for sharing on the Github. Releases will be made seasonally when there are major changes. Each program listing will have a brief description and instruction contained within this readme file. You can download the seasonal releases or you can download the individual program listings that you are interested in using on your calculator.

## Program Listing

Below you will find information on each program routine in this collection.

### Hours

HOURS is a program routine that allows the user to input a start time in H.m and a finish time in H.m which will produce the difference in H.m format. The program makes up for the lack of H.m <-> HR conversion and makes hourly wage calculations or time calculations extremely easy.

**Instructions:** Enter the start time in H.m (for example, 5.23) which will be stored in register 1, press ENTER to push the value to the y-register. Enter the end time in H.m (ex, 14.17) which will be stored in register 2, there is no need to press ENTER as the first and second value are properly stored in the y-register and x-register respectively at the commencement of program run. Now, if the listing is the first in your program line then press R/S, else you will need to press g GTO followed by the line number where the HOURS program listing starts and then R/S to start the program. Once complete the program displays the difference in H.m format (for our example, 8.54) which will also be stored in register 3. The values for the start and end times are stored in registers 1 and 2 in H.m format for RCL if needed by the user).

  001 STO 2 [44 2]
  002 R↓ [33]
  003 STO 1 [44 1]
  004 FRAC [43 24]
  005 . [48]
  006 6 [6]
  007 ÷ [10]
  008 RCL 1 [45 1]
  009 INTG [43 25]
  010 + [40]
  011 STO 1 [44 1]
  012 RCL 2 [45 2]
  013 FRAC [43 24]
  014 . [48]
  015 6 [6]
  016 ÷ [10]
  017 RCL 2 [45 2]
  018 INTG [43 25]
  019 + [40]
  020 STO 2 [44 2]
  021 RCL 1 [44 1]
  022 - [30]
  023 RND [42 14]
  024 STO 3 [44 3]
  025 FRAC [43 24]
  026 . [48]
  027 6 [6]
  028 × [20]
  029 RCL 3 [45 3]
  030 INTG [43 25]
  031 + [40]
  032 STO 3 [44 3]
  033 Clx [35]
  034 ENTER [36]
  035 ENTER [36]
  036 ENTER [36]
  037 RCL 3 [45 3]
  038 GTO 000 [43,33,000]

**Registers Used:** The following registers are used in the program during execution.

> - Register 1 Start time (H.m)
> - Register 2 End time (H.m)
> - Register 3 Difference (H.m)

### Wages

WAGES is a routine that allows the users to quickly calculate an hourly wage given the number of hours as an input in the x-register. The program can pair with the HOURS listing to provide two powerful tools for calculations relevant to hourly wage jobs. A bonus is that with these two routines loaded the total program listing is exactly 50 lines and you can GOTO line 040 (easy to remember given standard 40 hour work weeks) to calculate the wages.
