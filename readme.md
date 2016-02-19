FFmpegPlayer-iOS - A movie player for iOS based on FFmpeg.
==========================================================

### Build Instructions

First you need to download, configure and build [FFmpeg](http://ffmpeg.org/index.html).

Before that, edit the ``Rakefile`` and change the ``SDK_VERSION`` to the one you have installed. Look in the ``/Applications/Xcode.app/Contents/Developer/Platforms/iPhoneOS.platform/developer/SDKs/`` directory to find out what SDKs are existed in your OS

Build the ffmpeg:

	cd kxmovie
	git submodule update --init	
	rake

### Usage

1. Drop files from kxmovie/output folder in your project.
2. Add frameworks: MediaPlayer, CoreAudio, AudioToolbox, Accelerate, QuartzCore, OpenGLES and libz.dylib .
3. Add libs: libkxmovie.a, libavcodec.a, libavformat.a, libavutil.a, libswscale.a, libswresample.a

For play movies:

	ViewController *vc;
	vc = [KxMovieViewController movieViewControllerWithContentPath:path parameters:nil];
	[self presentViewController:vc animated:YES completion:nil];

See KxMovieExample demo project as example of using (see below).

Also, you can include kxmovie as subproject. Look at [kxtorrent](https://github.com/kolyvan/kxtorrent) as example.

Remember, you need to copy some movies via iTunes for playing them. And you can use kxmovie for streaming from remote sources via rtsp, rtmp, http, etc.

### Requirements

At least iOS 7.0 and iPhone 4 (because of iOS 7 requirements).

### Screenshots

<img src="https://raw.github.com/atelierdumobile/FFmpegPlayer-iOS/master/readme-media/screenshot-movie.png" alt="Movie View" width="50%">
<img src="https://raw.github.com/atelierdumobile/FFmpegPlayer-iOS/master/readme-media/screenshot-info.png" alt="Info View" width="50%">
<img src="https://raw.github.com/atelierdumobile/FFmpegPlayer-iOS/master/readme-media/screenshot-movie-landscape.png" alt="Movie View Landscape" width="50%">

### Runnning KxMovieExample project

First, ensure you have Pods installed. If not, exec this command:

    pod install

Steps to run the project:

* Open with xcode the kxmovie.xcworkspace.
* Select the KxMovieExample project in the active scheme display.
* Make sure bitcode is disabled in build settings.
* Build the project.
* Run the project in a connected mobile.

### Feedback

Tweet me — [@kolyvan_ru](http://twitter.com/kolyvan_ru).

Tweet me — [@MonsieurDart](http://twitter.com/MonsieurDart).
