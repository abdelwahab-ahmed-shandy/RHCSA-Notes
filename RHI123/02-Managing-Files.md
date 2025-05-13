# 📁 Chapter 2: Managing Files From the Command Line :
---

## 📌 Absolute paths and Relative paths: 

cd			 # Move to the current user's folder (home)
cd /root/Videos 	 # Move to an absolute path
cd Videos 	 	 # Move to a relative path within the home folder
pwd 		 	 # Display the current path
cd /root/Documents 	 # Move to another absolute path
cd ~abeer 		 # Move to the user's home folder abeer
cd - 			 # Go back to the previous folder
cd .. 			 # Move up a level
cd ../.. 		 # Move up two levels

---

## 📌 View files:

ls 		# Display directory contents
ls -l ~ 	# Display in long format
ls -a 		# Display all files, including hidden ones
ls -la 		# Display full long format
ls -lh 		# Display in long format with readable sizes
ls -R 		# Display directories recursively
ls -t 		# Sort by modification time
ls -r 		# Reverse sort
dir 		# Alternative command for ls
dir --color 	# Display in color

---

## 📌 Creating files:

touch file1 FILE1 		# Create files (case-sensitive)
touch /root/Documents/file 	# Create a file in a specific path
ls -R 				# Display files and folders recursively

---

## 📌 Create folders: 

mkdir dir1 dir2 dir3 	 # Create folders
mkdir -p dir4/dir5	 # Create a folder within a folder (nested)
mkdir 'A S' 		 # A folder with a name containing spaces
mkdir "A S"
mkdir A\ S

--- 

## 📌 Copy files and folders: 

cp file1 file2 				# Copy a file
cp file1 /root/Documents/ 		# Copy to a folder
cp file1 file2 file3 /root/Documents/   # The last path must be a folder
cp -r /etc/ dir1 			# Copy a non-empty folder
cp -r /etc/* dir1 			# Copy only the contents of the folder
cp ~/file1 . 				# Copy from home to the current folder

---

## 📌 Move/Rename:

mv file1 new_file1 			# Rename a file
mv file1 file2 file3 /root/Documents/   # Move multiple files
mv dir1 dir2 dir3 dir4 			# Move folders (destination must be a folder)

---

## 📌 Deleting files and folders:

rm file1 		# Delete a file (interactive as root)
rm -f file1 file2       # Force delete without confirmation
rm -d dir1 		# Delete an empty directory
rmdir dir1 		# Delete an empty directory (same purpose)
rm -rf dir1 		# Delete a non-empty directory with its entire contents

---

## 📌 Globbing:

touch alfa bravo charlie delta echo able baker cast dog easy
ls a* 		# Starts with a
ls *a 		# Ends with a
rm -f a* 	# Delete files that start with a
ls *a* 		# Contains a
ls [!a]* 	# Does not start with a
ls [ac]* 	# Starts with a or c
ls ???? 	# 4-letter names
ls ????? 	# 5-letter names

# Advanced examples:
touch file1 file2 file3 file4 file11 file12 file111 filea fileb fileab fa fab fabc

ls f? 		# 2-letter names starting with f
ls f?? 		# 3-letter names starting with f
ls file[a-c] 	# filea, fileb, or filec
ls file[^a-c] 	# Anything except a through c after file
echo ~abeer 	# Home path for user abeer

---

## 📌 Variables:

x=5
echo x 				# Prints "x"
echo $x 			# Prints "5"

echo "Today is $(date)" 	# Print the date within the line

echo "Sum of 1 plus 2 is $[1+2]"
echo "Sum of 1 plus 2 is $((1+2))"

---

### ✍️ Author: Abdelwahab Shandy









