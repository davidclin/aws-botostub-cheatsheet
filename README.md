# aws-botostub-cheatsheet
David Lin's AWS Botostub Cheatsheet

# GitHub repository
https://github.com/jeshan/botostubs

# Install Python3
Procedures below assume Python3 is already installed 

# Update OS
<pre>
sudo apt-get update
</pre>

# Create and activiate virtual environment
<pre>
virtualenv aws-vim-python3-botostubs-virtualenv
source aws-vim-python3-botostubs-virtualenv
</pre>

# Install boto3, botostubs, and jedi-vim binding to the jedi autocompletion library
<pre>
cd aws-vim-botostubs-virtualenv
pip3 install boto3
pip3 install botostubs
pip3 install jedi  <-- jedi-vim is a VIM binding to the autocompletion library jedi
</pre>

# Add following Plugin to .vimrc file
<pre>
Plugin 'davidhalter/jedi-vim'
</pre>

# Install jedi-vim using Vundle
<pre>
:PluginInstall
:PluginUpdate
</pre>

# Test 
Create then open test file named test.py in VIM (file extension is important)
<pre>
#!/usr/bin/python3
import botostubs
import boto3

s3 = boto3.  (the period should trigger autocompletion)
</pre>

# Get Help
from VIM, get help to jedi-vim via
  :help jedi-vim

# Update botostubs
botostubs is updated every 3 days
<pre>
pip install --upgrade botostubs
</pre>

# Resources
[botostubs Blog](https://www.awsadvent.com/2018/12/21/code-assistance-for-boto3-always-up-to-date-and-in-any-ide/)
Add more resources here
