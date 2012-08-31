## Contributing to LibShapeDraw

If you're an open-source Java developer looking to improve LibShapeDraw,
welcome! All reasonable pull requests are considered; feel free to fork and PR.

If you'd like to discuss potential major changes, you can open an issue on
GitHub or take it to IRC. (See the Contact section in the main `README.md`.)

Not a developer? No worries: any bug reports, feature requests, and general
comments are much appreciated. Please feel free to open an issue on GitHub.

Also if you're handy with graphic design, please contact me (bencvt)!
LibShapeDraw could use a logo. :)

## Building LibShapeDraw from source

If you just want to use the API in your own mod, feel free to skip this section
and use the prebuilt jar.

1.  Install [Maven](http://maven.apache.org/).
2.  Copy the contents of your Minecraft's `bin` directory to `lib`. Be sure to
    include the `natives` subdirectory; the test suite needs them.  
    `minecraft.jar` should be vanilla with only ModLoader patched in.
3.  Run Maven.

That's all there is to it. If you prefer to use an IDE, here's one way:

1.  Follow the above steps first, making sure everything compiles.
2.  Install [Eclipse](http://www.eclipse.org/) and a
    [Maven integration plugin](http://wiki.eclipse.org/M2E).
3.  Import the Maven project to your workspace.

## Tips and tricks

 +  You can enable debug dumps and tweak a few other global settings by copying  
    `libshapedraw/internal/default-settings.properties`  
    from the jar to the file system at  
    `<minecraft dir>/mods/LibShapeDraw/settings.properties`.

 +  If you're not using MCP or another system that provides a handy way to
    launch Minecraft in a dev environment (i.e., insulated from your actual
    Minecraft installation), see
    `src/test/java/launcher/StartMinecraftDev`.

## Development roadmap

Planned features, in no specific order:

 +  More built-in Shapes, perhaps with texture support as well.
 +  Mavenize Javadoc generation and publish them somewhere, probably GitHub.
 +  Improve JUnit test coverage.
 +  Expand the demos.
 +  Investigate the performance impact of making the API thread-safe, maybe
    provide a parallel implementation (LibShapeDrawThreadSafe).
 +  If there is community interest, add Forge compability.
 +  If there is community interest, make ModLoader/Forge optional. This would
    involve making a custom bootstrapper that modifies vanilla classes,
    basically a minimalistic built-in version of ModLoader.
 +  Add a plugin channel to allow servers to access the API on the client.
    The end user would be able to disable this feature if they'd rather not let
    the server draw shapes on their screen.
 +  Improved Trident animation library integration: built-in interpolators for
    types in libshapedraw.primitive.