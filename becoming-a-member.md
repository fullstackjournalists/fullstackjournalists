# Becoming a Member of Full Stack Journalists

Becoming a member of FSJ is easy. Attend one of our meetings, get your tools set up, and add yourself to the [member list](members.md)!

## Add yourself to the member list

### Fork the repository

Go to the [Full Stack Journalists repository](https://github.com/fullstackjournalists/fullstackjournalists). In the upper right, you will see a button that says 'fork.' Press that. You will need a free Github account and to be logged into that account for this to work.

### Clone the repository

Now you have your own copy of the repository at http://github.com/yourusername/fullstackjournalists/  You should already be on that page. You'll see a green button on the left that says 'Clone or Download.' Click that button. A dialog will open and you'll see a URL. copy that.

Open Terminal. Go to your projects folder (or wherever you want your new fullstackjournalists folder to be).

At the command line, type `git clone` and then paste the URL you copied.

Hit return.

### Navigate to your new /fullstackjournalists folder

At the command line, type `ls`. You'll see a list of all the folders and files in the directory you're currently in. You'll see a new folder called `fullstackjournalists`. At the command line, type `cd fullstackjournalists` and hit return. You are now in the `/fullstackjournalists` directory. Type `ls`. You'll see a list of files. The file you are looking for is `members.md`.

### Add yourself to the members.md file

Open `members.md` in your text editor. Add your name to the file.

### Commit your changes.

Once you've added yourself, save the `members.md` file. In terminal, type `git status`.
You should see a number of files, including your edited members.md. file.

Type `git add -A` and hit return to add all your files.

Type `git commit -m "adding my name to the member file"` and hit return.

Type `git push origin master`.


### Make a pull request.

Visit http://github.com/yourusername/fullstackjournalists and refresh the page. You should see your committed changes.  Look for the 'pull requests' tab. Click on it. Click the green 'Make New Pull Request' button. Make a little note, and then submit your pull request. Your changes will be integrated into the main /fullstackjournalists repository by an admin. 
