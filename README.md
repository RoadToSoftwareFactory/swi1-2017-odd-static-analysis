# swi1-2017-odd-static-analysis

1. Open the file named after you.
1. Each file should have 7 lines - these are the name of a method, and its location, under manageiq-ui-classic/app/controllers/
1. For each potentially dead method, look if it's really dead and add your findings to the file...


For example, for file:

```
dead_method    fake_controller.rb
undead_method    fake_controller.rb
```

you would mark `dead_method` as just `dead`, and add the place where `undead_method` is being used.

```
dead_method    fake_controller.rb
	dead
undead_method    fake_controller.rb
	alive - called from fake_controller#foobar
```

1. After you've gone through all the methods, commit the file (not on master!), and push it to github
1. Then create a PR with that updated file.
1. Edit the description of the PR - mention all the things you tried when looking for those methods.
