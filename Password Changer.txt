@echo off
title Password Changing Tool -RGJ

:MENU
echo 			Password Changing Tool -RGJ		Quit(Q)
echo.
echo.
echo	If and only if your password is lost the only use this software.
echo.
echo	NOTE:- I am not responsible for the misuse of the software...
echo.
echo.
echo	Do you want to contunie? (y/n)
CHOICE /c:ynq /n > nul
  if errorlevel 3 goto END
  if errorlevel 2 goto END
  if errorlevel 1 goto MENU1


:MENU1
cls
echo 			Password Chagning Tool -RGJ		Quit(Q)
echo.
echo.
net user
echo.
echo	Enter the user name of which you want to chage the password off : 
set/p "acc=>"
echo.
net user %acc% *
echo.
echo.
echo	Do you want to try again correctly? (y/n)
CHOICE /c:ynq /n > nul
  if errorlevel 3 goto END
  if errorlevel 2 goto END
  if errorlevel 1 goto MENU1

:END
