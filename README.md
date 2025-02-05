# Automatic_File_Sorter_Project_Python
Using Python to test my abilities to manage files and folders.

I used files in .csv, .txt, .png formats to test abilities of moving them to new folders.

First, I created the folders, then I moved the files to these folders, creating an automatic loop to not have to do it manually.

**********************************************************************************

path = r'C:\Users\gugaa\Documents\Python\Automatic File Sorter Project\\'

folder_names = ['CSV Files','Text Files','Image Files']

for folder in folder_names:
    if not os.path.exists(path + folder):
        os.makedirs(path + folder)

file_names = os.listdir(path)

for file in file_names:
    if ".csv" in file and not os.path.exists(path + "CSV Files\\" + file):
        shutil.move(path + file, path + "CSV Files\\" + file)
    elif ".txt" in file and not os.path.exists(path + "Text Files\\" + file):
        shutil.move(path + file, path + "Text Files\\" + file)
    elif ".png" in file and not os.path.exists(path + "Image Files\\" + file):
        shutil.move(path + file, path + "Image Files\\" + file)
