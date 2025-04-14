# CBT155
Converted to GitHub via [cbt2git](https://github.com/wizardofzos/cbt2git)

This is still a work in progress. 
Due to amazing work by Alison Zhang and Jake Choi repos are no longer deleted.

```
//***FILE 155 is from David North and contains two versions of      *   FILE 155
//*           the REXX reformatter exec.  In addition, there are    *   FILE 155
//*           other REXX execs, notably REXX8080, which can         *   FILE 155
//*           reformat VB-255 REXX execs so they can be made into   *   FILE 155
//*           FB-80 REXX execs that work the same way.              *   FILE 155
//*                                                                 *   FILE 155
//*  Subject:  REXXREF - Additional explanation                     *   FILE 155
//*  From:     "North, David (USI)" <david.north@unistudios.com>    *   FILE 155
//*                                                                 *   FILE 155
//*            Technical Services Group                             *   FILE 155
//*            Dave North                                           *   FILE 155
//*            3429 Downing Ave.                                    *   FILE 155
//*            Glendale, CA. 91208                                  *   FILE 155
//*                                                                 *   FILE 155
//* REXXREF and REXREF--------------------------------------------- *   FILE 155
//*     The two execs (ISPF edit macros) REXXREF and REXREF were    *   FILE 155
//*     written for VM CMS.  REXXREF is the full version, does      *   FILE 155
//*     reformatting and cross reference, and REXREF is the same    *   FILE 155
//*     with the cross reference code removed.  In both macros I    *   FILE 155
//*     disabled the VM code and replaced it with ISPF code.        *   FILE 155
//*     Not all of the options work, I have plans to make it all    *   FILE 155
//*     work.                                                       *   FILE 155
//*                                                                 *   FILE 155
//*     The default is to reformat and not attempt the cross        *   FILE 155
//*     reference.  It will indent 3 cols for each level of IF,     *   FILE 155
//*     DO, SELECT, etc.  Comments will be right adjusted to col    *   FILE 155
//*     73.  REXX reserved words will be capitalized with REXX      *   FILE 155
//*     functions in all caps.                                      *   FILE 155
//*                                                                 *   FILE 155
//* REXX8080------------------------------------------------------- *   FILE 155
//*                                                                 *   FILE 155
//*     Here is the atttempt at converting REXX VB-255 files        *   FILE 155
//*     into FB-80 with correct continuation, REXX8080.             *   FILE 155
//*     REXX8080  - 09/28/99 - Reformat REXX program into 80 col    *   FILE 155
//*                 lines by breaking up lines longer than 80       *   FILE 155
//*                 into continuation lines.  Note: line without    *   FILE 155
//*                 blanks or "(", ")", or "=" is not split.        *   FILE 155
//*                                                                 *   FILE 155
//*                 Run this exec from ISPF edit and then move      *   FILE 155
//*                 the edited file to a FB-80 PDS.  Let the        *   FILE 155
//*                 truncation happen,  It's OK.  Everything        *   FILE 155
//*                 past col 80 is now blank.  Run REXREF or        *   FILE 155
//*                 REXXREF after REXX8080 to make it look nice.    *   FILE 155
//*                 Then re-run REXX8080 because the                *   FILE 155
//*                 reformatting may make long lines.               *   FILE 155
//*                                                                 *   FILE 155
//*                 Use the file called JUNK to validate/test       *   FILE 155
//*                 REXX8080. First it must be moved to a FB-255    *   FILE 155
//*                 PDS and the lines concatenated back into long   *   FILE 155
//*                 lines(use SPLITJOIN).                           *   FILE 155
//*                                                                 *   FILE 155
//*        Note:  Please see File 187 for a program to convert      *   FILE 155
//*               CLISTs from VB-255 to FB-80 and vice-versa.       *   FILE 155
//*                                                                 *   FILE 155
//* OTHER STUFF---------------------------------------------------- *   FILE 155
//*     Here are some VM crutches:                                  *   FILE 155
//*     The SPLTJOIN exec is very useful when adding comments to    *   FILE 155
//*     REXX's.                                                     *   FILE 155
//*                                                                 *   FILE 155
//*     ALL(VM)   - Show only lines which containe the specified    *   FILE 155
//*                 string. If no argument is passed the issue a    *   FILE 155
//*                 RESET to show all lines in the file. Syntax     *   FILE 155
//*                 for the string is the same as the EXclude.      *   FILE 155
//*                                                                 *   FILE 155
//*     QQuit(VM) - Cancel and throw away the editing changes to    *   FILE 155
//*                 the file                                        *   FILE 155
//*                                                                 *   FILE 155
//*     SPLTJOIN  - (For the XEDIT folks)                           *   FILE 155
//*                 Split the line at the cursor location, OR, if   *   FILE 155
//*                 there are only blanks following the cursor      *   FILE 155
//*                 then Join the following line to the cursor      *   FILE 155
//*                 line at the cursor position                     *   FILE 155
//*                                                                 *   FILE 155
//*        Hint:  Set a PF key, maybe PF14, to execute the          *   FILE 155
//*               VMSPLIT macro then you can simply                 *   FILE 155
//*               position the cursor at the location of            *   FILE 155
//*               the SPLIT/JOIN and press PF14                     *   FILE 155
//*                                                                 *   FILE 155
```
