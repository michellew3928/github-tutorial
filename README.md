# GitHub Tutorial Project By Michelle Wu

## _Overview_  

* Using markdown syntax, display all of your knowledge about **Git** and **Github** in a single README file.  

## _Directions_

1. Fork and clone this repository.
2. Notice there are two files:  
    a. `README.md` is where you will find a template to use as a starting point for your tutorial.  This is where you'll do your work.  
    b. `directions.md` is where you will find these directions.
3. As you edit, make a commit every once in a while.  Don't forget to push!  

## _Topic_
### Git: 
  * Git is a version control that keeps track changes of codes you do in your resporitory by snapshotting it.
  * Git does not require github in order to work, it could work on its own.  
### Github:
  * Github requires Git in order to work.
  * Github is a websites where you could see every work that is saved into the account you mad that links to the website [**Github**] (https://Github.com/) 
  * Using Github, you could see changes made when you are coding 
### Inital Setup
1. First, type in a new tab [**Github**] (https://www.github.com/) 
2. Next, go to the upper corner of the website and click on "**Sign in**" 
    * Username (Hint: Use a real name existing with a couple of number)
    * Connect it to your email address that you would want to use 
    * Create a password (easy to remember but only you know)
3. Then, Choose "**Unlimited public repositories for free**"
4. Then, In "**Talior your experience**" section, click on check the box shows that you had applied
5. Join into your email you used to sign up for and verify your email
6. Finally you have an account to access to Github! You are all set to go!  
#### SSH Key
1. First, Go to your Github account
2. Next, right next to the plus sign is your profile and click the arrow going down to "**Settings**"
3. Then, on the left side of the screen find "**SSH and GPG keys**" and click on it
4. Then, The SSH Keys section, clicked "New SSH key" 
5. Go back to cloud 9 and on the top right corner there should be a setting icon for you to click on
6. On the left, click **SSH Keys**, and copy all the things in the grey box 
7. Go back to GitHub, put title as "**cloud9**" and paste everything to the **Key** box and click **Add SSH Key**
8. You are all set, cloud 9 and Github are connected!
5. After creating it, no touch anything on that tab
6. Go to into your Cloud 9 in a new tab 
    * first step: type **cd ~/workspace** (You are navigating into the parent directory= workspace)
    * second step: type **mkdir first-repo** (You are making a file in the parent directory)
    * third step: type **cd first-repo** (You are navigatng into the child directory of workspace) 
    * fourth step: type **git init** (Initializes git in the current directory and you are able to start editing)
    * fifth step: type **touch README.md**
    * sixth step: type **c9** (You are able to open up the README with this)
    * seventh step: There would be a new termial **(README.md)** that pops up right next to the termial you are using that **(bash)**
    * eighth step: You could type anything inside of the README.md but remember to **"commit add ."** at the bottom in the **bash tab**
    * ninth step: type **git commit -m "create README"**
### Repository setup
1. Go on [**Github**] (https://www.github.com/) 
2. Go to the top right corner plus sign and click a down arrow on right next your profile
3. Click on "**new repository**" 
4. Type your the repo name you choose to do
* ongoing workflow & commands
  * status, add, commit, push
  * When you are opening a filename.md after you could do **Git status**
    * _**Git status**_: To view the current files that are on the stage
  * If the filename.md appears to be red, it means it is no in the staging area which you would need to do **Git add .**
    * _**Git add .**_: Adds the entire directory/files to the staging area but will not add any deleted or renamed files to the stage
  * #### **You _must_ do add before you commit**
  * **Git commit**: you see different changes you made in the staging area
    *  each time you make a change, "screenshoting" is different. It wouldn't be to same every time because they would mean you didn't make any chnages to your coding.
 * lastly, you could "push" your local into your remote repository, know as git push
   * ** Git push**: any git commit you do to your coding from your local repo pushes to your remote repo
   * Remote repo= Github
  * As a first time pushing to the remote repo, You would do **Git Push -U Origin Master**, every other time there is no need to use this because you could just do GIt Push afterwards because the program remebers where the commits should be sent into which remote.
    * breaking down each words help to understand it easier
    * **Git**: git command
    * **Push**: the commits are moving from the local repo to the remote repo
    * **U**: This tells the command to where to send your changes to
    * **Origin**: location (which repo are we trying to send the commits to)
    * **Master**: default branch, you can't go any higher than that because if you do those you the private files you shouldn't be messing around with before Github gets messed up. 
 ### rolling back changes
  * undo edit/add/commit/push
   * **git checkout -- FILENAME**: remove any changes that is not located in the staging area
   * **git reset HEAD FILENAME** - Removes a file from the staging area
   * **git reset --soft HEAD~1**: Undo previous commit
     * doesn't touch any files in the staging area so it would be protected
  * **~<NUMBER>**: it shows you the number of committs you have undid  
  * **git reset HEAD~1**: undo previous commit
    * the oppsite of git reset --soft HEAD~1, you delete files from the staging area
  * **git reset --hard HEAD~1**:undo prvious commit
    * it could make chaanges to the file and delete files from the staging area
    * this is removed from the history 
  * **git reset --hard SHA**: changes would to be gone
    * if you do a commit with SHA and you do another commit, the changes would be removed away from history
 * **git revert SHA [...]**: it makes a commit that is the opposte of the commit that has SHA.
   * instad of removing changes from the history,  if you added files, it will remove them on the new commit.
_NOTE: for each command, you should explain:_

#### More Git Commands you may use for coding with GItHub  
* **pwd**:Print Working Directory:tells you where you are (the file path)
* **ls**: Lists the contents of your current directory 
* **cd**: Navigates to the directory 
* **mkdir**:Make directory
   * Example: mkdir nyc, you are making a folder for nyc
   * When you do mkdir brooklyn you are making files inside of the folder you created before it which is nyc
* **rmdir**: Remove only Directory with empty files 
   * Example: If you did rmdir brooklyn, it deletes the brooklyn and other files inside of it 
* **touch**:Touch file.extension: make a file with nothing inside of it
* **rm**:Rm file.extension: removes the file that are empty 
* **rm -rf**:It force  removes all non-empty directory.
   * It would ask you if you would really want to.  
* **mv (to rename)** Mv oldname.extension  newname.extension: the file could be rename to your preference
   * Example: mv orange apple, this chnages ornage file to apple file now
* **mv (to move)** mv source1 [source2, etc] destination/
Example: bay-bridge brooklyn/
   * You moved bay-ridge into brooklyn 
* **c9**: opens up the file
 * **git init**: Initializes git in the current directory
 * **rm -rf .git**: Un-initializes a folder
* **git add .**Adds the entire directory/files to the staging area but will not add any deleted or renamed files to the stage
* **git add --all**: Include all changes, including deleted files.Will add any deleted or renamed files
* **git push**: Pushes the commit from local to the remote repository
* **git diff**: Only works before you add the file
* **git log**:Shows a list of previous commits
    * Git log shows a list of previous commits that you have done
 * **q (while in git log)**:Press Q to quit
 * **git checkout -- FILENAME**: remove any changes that is not located in the staging area
 * **git reset HEAD FILENAME** - Removes a file from the staging area
* **git remote -v**:Tells where the commits would be send to 
    * V =verbose
    * Finding all the possible ways that could be done
## _Other Requirements_

### Use MD syntax _(headings, bold, italics, etc)_
  * #### _Italic_
    * first shift dash ( _ )
    * then type in the word that you want it to be italized
    * last you would need to do shift dash( _ ) again to see your word look different from all the other words
    * For example: I feel tired everyday after school. 
      * you want to make tired intalized, place ( _ ) (space) (tried) (space) ( _ ) to make this _tired_
  * #### Bold 
    * first place two asterisk ( ** ) by holding shift and then tap on the number 8 twice 
    * space then the word 
    * lastly, hold shift and press the number 8 twice
    * This would thicken and darken the word or phrase you are bolding
    * For example: I'm melting!!! 
      * I want to bold the entire thing ( ** ) (space) (word/phrase) (space) ( ** )
      * **I'm melting!!!!**
 * #### Header
   * When you do headers in coding you use a hastag (#) by doing shift then the number 3. 
   * the number of hastags changes the size of the words
   * one hastag Format( # word): is the biggest size
     * # Header
    * two hastage Format:( ## word)
      * ## Header
    * three hastags Format:(### word)
      * ### Header
    * fourth hastags Format:(#### word)
      * #### Header
    * five hastags Format:(##### word)
      * ##### Header
  * six hastags Format:(###### word)
     * ###### header
 * #### Links Format: []()
   * link text use brackets ( [ ] ),
   * then you wrap the link in parenthesis ( ( ) )
   * For example: Google and New York times
     * [Search for it](https://www.google.com/) or
     * #### [New York Times] (https://www.nytimes.com/)
 * #### Images 
   * format:!([ ])(( )) 
   * [ ] link text
   * ( ) URL to the image
   * the only difference bewtween coding images and links is that images has has ! in front. Everything else is the same. 
