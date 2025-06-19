

 # 🚀 Office 365 ProPlus Activation Script Guide

> ⚠️ **Warning:** This script attempts to activate Office 365 ProPlus via KMS servers. 

---

## 🔐 Step 1: Turn Off Windows Antivirus Temporarily

1. Open **Windows Security**.
2. Go to **Virus & threat protection**.
3. Click **Manage settings** under "Virus & threat protection settings".
4. Turn **Real-time protection** to **Off**.

**Note:** Don't forget to turn it back **on** after running the script!

---

## 💾 Step 2: Save the Script as a `.cmd` File

1. Open **Notepad**.
2. Paste the following code:

``` @echo off
title Activate Office 365 ProPlus for FREE - MSGuides.com&cls&echo ============================================================================&echo #Project: Activating Microsoft software products for FREE without software&echo ============================================================================&echo.&echo #Supported products: Office 365 ProPlus (x86-x64)&echo.&echo.&(if exist "%ProgramFiles%\Microsoft Office\Office16\ospp.vbs" cd /d "%ProgramFiles%\Microsoft Office\Office16")&(if exist "%ProgramFiles(x86)%\Microsoft Office\Office16\ospp.vbs" cd /d "%ProgramFiles(x86)%\Microsoft Office\Office16")&(for /f %%x in ('dir /b ..\root\Licenses16\proplusvl_kms*.xrm-ms') do cscript ospp.vbs /inslic:"..\root\Licenses16\%%x" >nul)&(for /f %%x in ('dir /b ..\root\Licenses16\proplusvl_mak*.xrm-ms') do cscript ospp.vbs /inslic:"..\root\Licenses16\%%x" >nul)&echo.&echo ============================================================================&echo Activating your Office...&cscript //nologo slmgr.vbs /ckms >nul&cscript //nologo ospp.vbs /setprt:1688 >nul&cscript //nologo ospp.vbs /unpkey:WFG99 >nul&cscript //nologo ospp.vbs /unpkey:DRTFM >nul&cscript //nologo ospp.vbs /unpkey:BTDRB >nul&cscript //nologo ospp.vbs /inpkey:XQNVK-8JYDB-WJ9W3-YJ8YR-WFG99 >nul&set i=1
:server
if %i%==1 set KMS=kms7.MSGuides.com
if %i%==2 set KMS=kms8.MSGuides.com
if %i%==3 set KMS=kms9.MSGuides.com
if %i%==4 goto notsupported
cscript //nologo ospp.vbs /sethst:%KMS% >nul&echo ============================================================================&echo.&echo.
cscript //nologo ospp.vbs /act | find /i "successful" && (echo.&echo ============================================================================&echo.&echo #My official blog: MSGuides.com&echo.&echo #How it works: bit.ly/kms-server&echo.&echo #Please feel free to contact me at msguides.com@gmail.com if you have any questions or concerns.&echo.&echo #Please consider supporting this project: donate.msguides.com&echo #Your support is helping me keep my servers running everyday!&echo.&echo ============================================================================&choice /n /c YN /m "Would you like to visit my blog [Y,N]?" & if errorlevel 2 exit) || (echo The connection to my KMS server failed! Trying to connect to another one... & echo Please wait... & echo. & echo. & set /a i+=1 & goto server)
explorer "http://MSGuides.com"&goto halt
:notsupported
echo.&echo ============================================================================&echo Sorry! Your version is not supported.&echo Please try installing the latest version here: bit.ly/odt2k16
:halt
pause >nul ```


3. Save it as `activate.cmd`.
   - Set **Save as type**: All Files
   - Choose a location like Desktop

---

## ⚙️ Step 3: Run the Script as Administrator

1. Right-click on the `activate.cmd` file.
2. Choose **Run as administrator**.
3. Accept any **User Account Control (UAC)** prompts.

---

## ✅ Done!

Office should now attempt to activate. Be sure to **re-enable your antivirus** after running this file.

---

**Disclaimer:** This script and its method of activation are not endorsed by Microsoft. Use for educational or testing purposes only.

