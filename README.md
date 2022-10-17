Note from Mason (Forker):

This extractor is being used by me as an internal component for an MC project I have been working on. 
I forked it because the original had a quirk that interfered with said project's toolchain (that quirk being the 
files weren't allowed to be downloaded into an IntelliJ resources folder, because it blocks you from trying to 
download things into pre-exisiting directories). 

I do not intend on updating it beyond this fix. If you want to download it from here and using it, that's fine, 
but I would prefer if you downloaded the source code from the original developer, rmheuer. You can click the "forked
from" link to get to his original repository. 


# McAssetExtractor

#### About
McAssetExtractor is a tool to extract assets from Minecraft by
downloading from Mojang's API. It uses [GSON](https://github.com/google/gson)
to parse the API's JSON responses.

The [wiki.vg](https://wiki.vg) page on [Game files](https://wiki.vg/Game_files)
is a helpful resource to understand how this works.

The primary goal of McAssetExtractor is to provide a convenient way
to obtain Minecraft's assets while avoiding copyright issues. By
providing a tool to download assets from Mojang, we avoid any
potential copyright issues from distributing Minecraft's assets.

#### Building

Make sure you have Apache Maven installed, then run `mvn package`
to build. The output JAR will be found in the `target/` directory.

#### Running

McAssetExtractor requires Java 1.8 or higher. Use
`java -jar McAssetExtractor-1.0-jar-with-dependencies.jar <version> <destination>` to extract
assets, replacing `<version>` with your desired version, and
`<destination>` with a path to the destination directory.
You can use the latest release or snapshot by setting the version to
`latest` or `latest-snapshot`, respectively.

This should give an output similar to the following:
```
Downloading assets for version 1.19
Extracting assets from client JAR
...
Downloading assets from launcher meta
...

Summary:
Extracted XXX assets from JAR
Extracted XXX assets from launcher meta
```

If any errors are present, make sure you are connected to the
internet, and that you have specified a valid version and
output directory.
