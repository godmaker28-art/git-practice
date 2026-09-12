import os
import shutil

folder_path = input("Folder Path: ")
folder_paths = ["Images", "Documents", "Videos", "Others"]

try:
    if os.path.exists(folder_path):
        list_of_items = []
        list_of_items.append(os.listdir())
        image = 0
        docs = 0
        vids = 0
        others = 0
        
        for f_paths in folder_paths:
            if not os.path.exists(f_paths):
                os.mkdir(os.path.join(f_paths))

        if list_of_items.endswith(".png", ".jpg", ".jpeg", ".gif"):
            for list in list_of_items:
                    print(list)
        elif list_of_items.endswith(".pdf", ".docx", ".txt", ".pptx"):
            for list in list_of_items:
                    print(list)
        elif list_of_items.endswith(".mp4", ".mov", ".avi"):
            for list in list_of_items:
                    print(list)
        else:
            for list in list_of_items:
                    print(list)
except:
        if folder_path not in os.listdir():
            print(f"{folder_path} Does Not Exist!")
