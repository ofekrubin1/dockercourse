The two files in this directory are .bashrc and .aliasrc.

If you want to use them, you have to move them to your home dir.

I recommend, before doing that, save the old .bashrc that you have in your directory.

So - run the following commands (more or less):

#assuming you are in the bashrc_dir directory

mv ~/.bashrc ~/.bashrc_sav  # saving
cp .bashrc .aliasrc ~       # copying these two file to home dir (~ is home dir)
cd                          # change dir to your home
source .bashrc

# last update: 9/11/22  Tzvi

