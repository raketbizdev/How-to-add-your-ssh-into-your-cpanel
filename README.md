# How-to-add-your-ssh-into-your-cpanel

Many of us think of accessing our cpanel via ssh so heres how you can do it.
1. Open cpanel www.yourdomain.com/cpanel or www.yourdomain.com:2083.
2. Go to **security** tab.
3. Click **ssh Access**.
4. A new windows will open then click the **Manage SSH Keys**.
5. Another window will open this time click **Import Keys**.
6. in **import SSH Key** windows add a name of your ssh key the default is id_rsa.
7. before you can import the key you will go to your local computer and open terminal if you are using mac or linux machine but if you using window make sure you have putty installed.
8. Open terminal and type this to find your id_rsa
```
$ cd ~/.ssh/
```
9. then type this
```
$ cat id_rsa.pub
```
10. copy the code from the terminal usually it start with.
```
ssh-rsa 
```
for easy copy use this code instead
```
$ pbcopy ~/.ssh/id_rsa.pub
```
11. go back to the cpanel and paste the copied code under **Paste the public key into the following text box:**.
12. then click import 
13. Before closing the terminal go back Manage SSH under security and under Public Keys click **manage**.
14. then click **authorized** then close and your done.
15. to check if you can access the cpanel using terminal type this
```
$ ssh servername@yourdomain.com
```
where servername is usualy the name of your domain.
