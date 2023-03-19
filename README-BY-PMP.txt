as it is not clear where the output of an ant task invoked from idea's 'ant' tool window goes (in some cases, e.g. SimplePriorities), the following approach was invented.
update: the output of an ant task started from 'ant tool window' goes to 'messages' tool window that is not visible sometimes,
but can be activated by 'ctrl+4' or from 'view\tool windows' menu.
but you still need to 'build' module before trying to access its classes.

1. build module via 'ant' tool window, *.class files should appear after that.
2. add 'ant target' run config and specify needed task.
3. remove 'build' from 'before launch' list.
4. save the run config and launch it as usual.

some libs are stored as project files as they're not available on mvnrepo.
the paths to them are in build.xml files of submodules using them.
as they are absolute and hardcoded accordingly to d:\dbg path of home machine they have to be modified accordingly on other machines using this project.