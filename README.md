# DEWPA - Development environment for WordPress with Automation

This is a Vagrant configuration designed for development of WordPress plugins, themes, or websites (<http://vccw.cc/>) enhanced by the automation described in Udemy course "Become a Wordpress Develope: Unlocking Power with Code" by Brad Schiff (<https://www.udemy.com/course/become-a-wordpress-developer-php-javascript/>).

Setting up the DEWPA

1. Install VirtualBox.

    <https://www.virtualbox.org/>

2. Install Vagrant.

    <http://www.vagrantup.com/>

3. Istall Node.js.

    <https://nodejs.org/>

4. Create and change into a directory, where you want to have the DEWPA

5. Download, unpack and move the DEWPA files to the directory created in previos step (dewpa directory of .zip file is not necessary).

    <https://github.com/petrsahula/DEWPA/blob/master/download/dewpa.zip>

6. Run the terminal/CLI and move to the directory created in step 4

7. Install the vagrant-hostsupdater plugin. (Optional)

    $ vagrant plugin install vagrant-hostsupdater

Important!!
Windows does not allow to change hosts files. Please add vccw.test 192.168.33.10 by yourself!

8. Download vagrant box

    $ vagrant box add vccw-team/xenial64

9. Start a Vagrant environment.

    $ vagrant up

10. Visit WordPress on the Vagrant in your browser and check the virtual environment.

    <http://vccw.test/> or <http://192.168.33.10/>

Environments
WordPress

This tool installs a WordPress environment with these settings by default.

    Default user
        Username: admin
        Password: admin

MySQL

    MySQL Host: 127.0.0.1
    Username: wordpress or root
    Password: wordpress
    Port: 3306

SSH

    Host: vccw.test or 192.168.33.10
    Username: vagrant
    Password: vagrant
    Port: 22

You can login virtual machine with vagrant ssh.

By this step you have finished the installation of the wordpress running in the virtual environment on your computer. If you want to install the full automation for your development environment, continue with the following steps.

11. Check that the node and npm are working.

    $ node --version

    $ npm --version

12. Install and check the gulp

    $ sudo npm install gulp-cli -g

    $ gulp --version

13. Install node packages

    $ sudo npm install

14. Check/change the path in setting.js to direct to the theme you are going to work on
    exports.themeLocation = './wordpress/wp-content/themes/theme-you-are-going-to-work-on/';

    $ nano setting.js

15. Start gulp and test if the page in browser is reloaded after saving .php and changing after saving .css and .js files in the theme directory.

    $ gulp watch

Automatization works on gulp links only:

    Local: http://localhost:3000
    External: http://your_network_IP:3000
    (Your external IP is generated and shown on the screen after you run gulp watch.)

    and 

    UI: ...:3001


AND enjoy, you are done.