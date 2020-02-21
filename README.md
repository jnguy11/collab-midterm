# midterm
Git pull:
pulls down from a remote for what you tell it to and instantly merges it into the branch you're currently on when you make the request.
Pulling will copy from the original and actually transfer data to the remote repo

You would do git pull to obtain all the changes done to the original to your local repo.

git fetch: 
tells your local git to retrieve the latest data from the original of a cloned project. but does not do any actual file transfering, it checks to see if any changes were made.

You would git fetch to check for any changes done in a remote repo or branch since your last pull before actually doing a pull which could result in a loss of data.

git clone:
Allows you to copy someones open-source project and create a local repo on your machine to work on the project in a separate repo on github without actually affecting that person's main repo.

Real life situation would be me cloning the collab midterm repo from Armaan and creating my own local-repo with the project as well as creating my own github repo to work on and save changes to my own repo. This will not affect Armaan's repo whatsoever.

| Trello                        |     Asana            |
| ------------------------------|:--------------------:|
| Allows for boards, lists, and cards| Allows for projects, lists, and tasks      |
| Allows up to 10 team members       | Allows up to 15 team members       |
|Cannot chat and message with team members | Has a chat/ messaging function  |
| Better for smaller teams| Better for bigger teams        |
| Only the one format                 | Calendar format|
| No email integration       | email integration    |

### Section 3

##### Question 1 What is the .git folder? Where is the object database in this folder?

Git golder contains all necessary info for your project which incljdes commits, remote repo address, and a log
which stores commit history, allowing for a user to roll back to history.
The object database inside the .git folder is within the objects directory.

#### Question 2 Explain in detail how the git hash-object function works.

The hash-object function is a one way function. A hash can be created based on an input but you cannot take the hash and convert it back into the original input. Git uses a SHA-1 hash, resulting in a 40-cahracter checksum hash.
Once you use hash-object function, it will write the resulting object into the object database, storing it in the directory, with the -w tag. The hashed-object must be staged and committed.
You can find the hashed object inside the .git/objects folder. The firwst two characters of the hash will be the folder name it creates, with the remaining being inside that folder.

#### Question 3: Where does git internally store the file names to our files? How are tree objects related to this?

file names are stored inside the .git/objects directory, with the first two characters of the hash being the directory. eg. hash starts with 1f, resulting directory will be ./git/objects/1f/(remaining hash characters)

Tree objects are related in the sense that they contain pointers to blobs and other trees, representing the contents of a directory or subdirectory.