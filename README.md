# Installation Of Windows 11 On VMware Fusion
## Prerequisites 
- You must have installed VMware Software (You can use VMware Workstation for Windows OS)
- You must have .iso file of windows 11 (You can download from microsoft's official website)

### 1. Start VMware and click on add VM.
<img width="550" alt="Screenshot 2022-07-19 at 4 32 55 PM" src="https://user-images.githubusercontent.com/74067699/179740498-bbd17f45-7e5b-4d55-9dd2-18ab0f58148e.png">

### 2. Go to Create Custom Virtual Machine.
<img width="550" alt="Screenshot 2022-07-19 at 4 33 03 PM" src="https://user-images.githubusercontent.com/74067699/179740821-c3aa0162-6d5e-4240-99ac-e102f3295e91.png">

### 3. Choose OS you want to install, Choose Microsoft Windows > Windows 10 and Later.
<img width="550" alt="Screenshot 2022-07-19 at 4 33 14 PM" src="https://user-images.githubusercontent.com/74067699/179741076-d75a0f47-5cb2-4c29-8efd-d339beff0902.png">

### 4. When choosing Firmware Type choose UEFI because we will be working on Windows and it's file system(NTFS) works on UEFI.
<img width="550" alt="Screenshot 2022-07-19 at 4 33 31 PM" src="https://user-images.githubusercontent.com/74067699/179741363-1e52c0db-2e96-4c97-b844-eb18df74ed45.png">

### 5. Now choose virtual disk here we are doing for first time so we'll create new virtual disk. Also you can increase or decrease capacity later.
<img width="550" alt="Screenshot 2022-07-19 at 4 33 37 PM" src="https://user-images.githubusercontent.com/74067699/179742187-b1e71366-b7c4-40a8-9b5b-d4293585016c.png">

### 6. Here, you can see what you've choosen to install Windows 11 into VM and you can specify path where you want to install your VM.
<img width="550" alt="Screenshot 2022-07-19 at 4 33 46 PM" src="https://user-images.githubusercontent.com/74067699/179742528-b4f64447-b092-464e-b93e-4cfc9fdf3cd8.png">

### 7. After doing all these thing click on finish and you will get prompt to this window.
<img width="550" alt="Screenshot 2022-07-19 at 4 35 04 PM" src="https://user-images.githubusercontent.com/74067699/179742854-6125de86-63d1-4e5b-bc82-96afff0aed84.png">

#### Here you can configure your VM how to behave, you can change Network Interface, Disk Capacity, RAM and Most Important Attach ISO file to VM,let's do this.

### 8. Give your VM RAM you want to give but it's better to give recommended capacity for good performance.
<img width="550" alt="Screenshot 2022-07-19 at 4 35 18 PM" src="https://user-images.githubusercontent.com/74067699/179743961-aa786fdf-6a5b-4385-ba0d-f8168b7775d4.png">

### 9. Select network interface for your VM.
<img width="550" alt="Screenshot 2022-07-19 at 4 35 32 PM" src="https://user-images.githubusercontent.com/74067699/179743978-ad9dacc4-edea-49d0-8994-c960945a4b60.png">

### 10. Specify storage capacity.
<img width="550" alt="Screenshot 2022-07-19 at 4 35 47 PM" src="https://user-images.githubusercontent.com/74067699/179744019-df5c16b8-c5af-4c4b-8c68-1090795a9b97.png">

### 11. This is important one choose ISO file it is ultimately your image of OS you've downloaded from Microsoft website specify the path where you've put your ISO file and Check the chekbox on top left.
- If you do not check this check box your VM could not be start with windows 11
<img width="550" alt="Screenshot 2022-07-19 at 4 35 59 PM" src="https://user-images.githubusercontent.com/74067699/179744049-14a30840-0529-4306-8c32-1945be70fe6f.png">

<img width="550" alt="Screenshot 2022-07-19 at 4 36 11 PM" src="https://user-images.githubusercontent.com/74067699/179744077-0feeea6c-a4a6-473e-bbf9-b452fe210fae.png">

### 12. Now you'll see this window click on play button.
<img width="550" alt="image" src="https://user-images.githubusercontent.com/74067699/179757435-25cd5bf5-1eaa-4ff7-bab8-13e93269b0cb.png">

### 13. After this you will see windows started booting.
<img width="550" alt="image" src="https://user-images.githubusercontent.com/74067699/179758211-9b5284ae-f3c2-4470-a616-f8239f5204be.png">

### 14. You'll see this windows which is very common when you install windows OS into system.
<img width="550" alt="image" src="https://user-images.githubusercontent.com/74067699/179758527-2737c0b8-5a10-4bac-b0de-0dba60d1475c.png">

<img width="550" alt="image" src="https://user-images.githubusercontent.com/74067699/179758560-533b67eb-e7bc-4584-9801-f36fbb8c92a8.png">

<img width="550" alt="image" src="https://user-images.githubusercontent.com/74067699/179758600-17fa7f7c-7cb9-43c6-97c2-7901a5bd205b.png">

<img width="550" alt="image" src="https://user-images.githubusercontent.com/74067699/179758620-4d15b8b7-0158-40f5-8a43-66d3425eaf2a.png">

### 15. This Error happens,
<img width="550" alt="image" src="https://user-images.githubusercontent.com/74067699/179758655-bf8130db-7bab-4f62-a250-3cdd5141d5b6.png">

### 16. Now comes to important part system is not allowing you to install windows 11 is becuase TPM/SecureBoot check, so we have to Bypass this checks by making some changes in registry.
- Press Shift + F10 to open Command Prompt
<img width="550" alt="image" src="https://user-images.githubusercontent.com/74067699/179807296-d4dae636-cf6f-4952-980a-a7c376398d8d.png">

```shell 
X :\Sources>regedit
```
- use regedit command to open registry
<img width="550" alt="image" src="https://user-images.githubusercontent.com/74067699/179807807-fba20e2d-9ddc-4cfa-9181-819834dfef2d.png">

### 17. After opening Registry editor go to following path
```shell
Computer\HKEY_LOCAL_MACHINE\SYSTEM\Setup
```
<img width="550" alt="image" src="https://user-images.githubusercontent.com/74067699/179808447-1596b3cb-16b1-4089-b3d7-664b45b0221d.png">

### 18. Now, right click on screen and create new key as following
- Name it "LabConfig" create New DWORD(32-bit) Value called "BypassTPMCheck" and Modify Value Data to 1

<img width="550" alt="image" src="https://user-images.githubusercontent.com/74067699/179809295-34c2131e-d3b4-4b94-b788-89ba9f9c79e4.png">

<img width="550" alt="image" src="https://user-images.githubusercontent.com/74067699/179809322-66677499-3d42-4892-ac1e-8a169726a463.png">

<img width="550" alt="image" src="https://user-images.githubusercontent.com/74067699/179809343-71ddbce9-786c-4e52-b5a5-45b4960025e2.png">

<img width="450" alt="image" src="https://user-images.githubusercontent.com/74067699/179809367-b4b30cf7-bc3d-4c2e-ab2d-f3d86861d400.png">

### 19. Add two more DWORD(32-bit) Value called "BypassRAMCheck" and "BypassSecureBootCheck" and Modify Value Data to 1 
- Be careful with spelling

<img width="550" alt="image" src="https://user-images.githubusercontent.com/74067699/179809910-a73380c4-28f1-40ef-a5f2-a0cdd8cccb28.png">

### 20. After following these steps close the window saying 'this Pc can not run windows 11' and Install windows again, This time at the end you'll get this window

<img width="550" alt="image" src="https://user-images.githubusercontent.com/74067699/179810403-d8a08338-b2b1-4061-9b49-856a5b9b0cb7.png">

### 20. Accept the agreement and click on next and follow this steps.

<img width="550" alt="image" src="https://user-images.githubusercontent.com/74067699/179810751-97f34f36-f9d9-4fde-a6d2-7cce51a66871.png">

<img width="550" alt="image" src="https://user-images.githubusercontent.com/74067699/179810783-816cb7a1-924b-48f9-b858-04998e723f53.png">

### After getting this prompt windows is finally started intalling. Wait for some minutes

<img width="550" alt="image" src="https://user-images.githubusercontent.com/74067699/179811478-f6515666-85f0-4329-bdcc-617d34920fd9.png">

### When Windows 11 finally got install in your VM you'll get this

<img width="500" alt="image" src="https://user-images.githubusercontent.com/74067699/179811635-e83e8f21-d1a8-42e4-972f-dc34c2444bd0.png">

- From now you can set-up windows by your own.
- This is the way you can configure your VM to run as Windows 11 computer.
