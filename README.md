Note from Mason (Forker):

This extractor is being used by me as an internal component for an MC project I have been working on. 
I forked it because the original had some quirks involving its download process that interfered with my 
project's toolchain. (In short, the original downloads the asset files into a folder named "assets", while the 
assets in my project need to be downloaded into a folder named "resources". There was also a problem with downloading
the assets into an existing folder, which I've patched).

I do not intend on updating it beyond the changes I need for the above. This fork is not really intended for end-users,
as the changes I've made are tailored to the aforementioned project's structure. If you want to download it from here and use it, 
that's fine, but I would prefer if you downloaded the source code from the original developer, rmheuer. 
You can click the "forked from" link to get to their original repository. 


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

Download the code and import into your IDE, Gradle should handle the rest from there.

#### Running

McAssetExtractor requires Java 1.8 or higher. Use
`java -jar McAssetExtractor-1.0_02-jar-with-dependencies.jar <version> <destination>` to extract
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
