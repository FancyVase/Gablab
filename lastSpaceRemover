import os

# Place lastSpaceRemover in folder with TEST_SUBJECT folders
# Replace "path" with that folder path
path = '' 
fileList = []
fileTuple = ('.txt') # Holds the filename terminations that we want
numTuple = ('0','1','2','3','4','5','6','7','8','9')

# Searches root folder and folders within the path for files ending in the terminations from fileTuple
for root, dirs, files in os.walk(path):
    for file in files:
        if file.endswith(fileTuple):
        	file_directory = (os.path.join(root, file))
        	fileList.append(file_directory)

# Will check if file ends with a number from numTuple, if not, it will remove the blank space
for directory in fileList:
	f = open(directory, 'r+')
	content = f.read()
	if not content.endswith(numTuple):
		with open(directory, 'rb+') as filehandle:
			filehandle.seek(-1, os.SEEK_END)
			filehandle.truncate()
