BACKGROUND
==========

My real problem resolves a configuration to grab a rules file. Another plugin modifies the publication block to add some data to the pom/ivy files.

If the project has a sort of cycle B depends on `compile project(':a')`, A depends on `testCompile project(':b')` I see this error.

    > A problem occurred configuring project ':a'.
    > Cannot configure the 'publishing' extension after it has been accessed.

Is there a better way to accomplish this. Is there a way to loop over all publications outside of doing it in afterEvaluate?
