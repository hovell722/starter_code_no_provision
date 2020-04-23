# Node App

This repo will allow you to set up Virtual Machines, that will allow you to run an app, connected to a database. If the app runs you will be able to view it on your internet browser with the address ``development.local``

## Dependencies

To use this app you need:
- vagrant
- Virtual Box

All other dependencies should be installed in the provision.sh folders, when setting up.

## How to use

To start the virtual machines:
```
$ vagrant up
```
Enter your password when prompted.

Once your vagrant has set up, go into `tests/spec` and test using the command:
```
$ rake spec
```

If all pass, the app and database are set up correctly.

To start the app go into to app machine:
```
$ vagrant ssh app
```
Then start the app:
```
$ cd /home/ubuntu/app

$ npm install

$ npm start
```
Use `npm test` to check if all ``development.local`` pages will work. if posts fails, that means the database is not connected correctly.

You should then be able to access ``development.local`` to see the homepage.

You can also access pages ``development.local/posts`` and ``development.local/fibonacci/{index}``, where {index} can be any number and will return you a value within the fibonacci sequence.
