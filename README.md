# Python.lesson.7.py


Задание 1:


# define dub folders

sub_folder_set = {

    "AoW",
    
    "CSP",
    
    "Folder A",
    
    "Folder B",
    
    "Folder C",
    
    "Folder D",
    
    "Folder F",
    
    "Folder E",
    
}



for group, people in group_person_dict.items():

    g = str(group)
    
    for p in people:
    
        # obtain name+group concatanated string
        
        folder_name = f"TutorGroup={g}-Person={p}"
        
        # build main directory path, create if not exists
        
        dir_path = os.path.join(dirname, folder_name)
        
        if not os.path.exists(dir_path):
        
            os.mkdir(dir_path)
            


        # iterate ovr subfolders
        
        for sbf in sub_folder_set:
        
            # obtain sub directory path, create if not exists
            
            subdir_path = os.path.join(dir_path, sbf)
            
            if not os.path.exists(subdir_path):
            
                os.mkdir(subdir_path)
                
                
                
Задание 3:


main.py

|---foo

    |---__init__.py
    
    |---bar.py
    
    
from bar import worker


def worker():

    pass
    

import foo.bar

foo.bar.worker()



import foo

foo.worker()




Задание 4:



import os

directory = r'my_direct'



for f in os.listdir(directory):

    path = os.path.join(directory, f)
    
    if os.path.isfile(path):
    
        print(os.path.getsize(path))
        
        
        
list = os.listdir(directory)

number_files = len(list)

print(number_files)      
