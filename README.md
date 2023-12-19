# 📌 bash

 Bash commands allow us to perform common tasks like creating, editing, deleting files and folders through the command-line interface (CLI).

## Easy navigation

- [Working with files and directories](#task-1)
- [Editing files, checking and killing proccesses, working with websites](#task-2)

## Task 1

##### Working with files and directories
```bash

# Home directory 

cd ~

# Show current directory path

pwd

# Create a directory named test1

mkdir test1

# Go to directory test1

cd test1


# Create file 1,2 and 3 inside directory test1

touch file_1 file_2 file_3


 # Check directory test1 content

ls


 # Check directory test1 content

cd ..

# Create directory test2 inside home directory

mkdir test2


# Delete directory test2

rm -r test2


# Delete file 2 from directiry test1

rm test1/file_2


# Create directory test3 & Add two files to directory test3

mkdir test3
cd test3
touch file_1 file_2


# Delete directory test3 

rm -r test3


# Create directory test4

mkdir test4


# Move file1.txt and file3.txt from directory test1 to directory test4

mv test1/file_1 test1/file_3 test4


# Add 3 lines to file1.txt

echo "line 1" >> test4/file_1
echo "line 2" >> test4/file_1
echo "line 3" >> test4/file_1


# Check content of file1.txt

cat test4/file_1

# Add 3 lines to file3.txt

echo "line 1" >> test4/file_3
echo "line 2" >> test4/file_3
echo "line 3" >> test4/file_3


# Check contents of file1.txt and file3.txt at once

cat test4/file_1 test4/file_3


#Using one of the editors, replace all lines in file 1

nano test4/file_1
 
```
## Task 2
##### Editing files, checking and killing proccesses, pinging websites
```bash
#Go to home directory

cd ~

# Create directory test3 

mkdir test3


# Add 3 files to test3, each of which should contain 4 lines

echo "row1" > test3/file_4
echo "row2" >> test3/file_4
echo "row3" >> test3/file_4
echo "row4" >> test3/file_4

echo "row1" > test3/file_5
echo "row2" >> test3/file_5
echo "row3" >> test3/file_5
echo "row4" >> test3/file_5

echo "row1" > test3/file_6
echo "row2" >> test3/file_6
echo "row3" >> test3/file_6
echo "row4" >> test3/file_6



# Find the line "row2" in file5.txt

 grep "row2" test3/file_5

# Find the line "row" in the test3 directory

grep "row" test3/*



# Count number of lines containing word "row" in file6.txt

grep -c "row" test3/file_6


# Find file5.txt in test3 directory

find test3 -name "file_5"

# Using find command delete file5.txt

find test3 -name "file_5" -delete

# Using the echo command, add the word "test" to file4.txt

echo "test" >> test3/file_4



# Change the word "test" in file4.txt to "fail"

sed 's/test/fail/' test3/file_4

# Add the word "test" to file4.txt so that the content is preserved

echo "test" >> test3/file_4



# View all processes in the system

ps aux

# Kill process 666 in console

kill 666

# Check the availability of the website artsiomrusau.com using ping

ping artsiomrusau.com

# Send 5 packages to artsiomrusau.com

ping -c 5 artsiomrusau.com

# Using GET and cURL command, get info about registered pets at petstore.swagger.io

curl -X 'GET' \
  'https://petstore.swagger.io/v2/pet/findByStatus?status=available' \
  -H 'accept: application/json'

# Using POST and cURL command, create a new user at petstore.swagger.io
curl -X 'POST' \
  'https://petstore.swagger.io/v2/pet' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
  "id": 0,
  "category": {
    "id": 0,
    "name": "string"
  },
  "name": "doggie",
  "photoUrls": [
    "string"
  ],
  "tags": [
    {
      "id": 0,
      "name": "string"
    }
  ],
  "status": "available"
}'


```
