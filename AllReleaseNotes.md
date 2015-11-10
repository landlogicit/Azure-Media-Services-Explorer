Version 3.32.0.0 brings the following features and improvements :

* **New bulk ingest manifest feature** (in transfers tab). Useful if you want to upload assets with an another client application (like Aspera or Signiant). Upload is decoupled from Azure Media Services asset creation. Any application that copies files to Azure Storage can be used.
  * a new UI to select files or folder to upload, and to organize the destinations assets
  * support for local storage encryption before the upload
  * tested with Cloudberry Explorer
* Support for **new Media Processors** (private preview)
* Adds two **audio only profiles** for Media Encoder Standard (MES)
* Support for **Hyperlapse with a speed of 1** (stabilization)
* **Optimization for large number of assets or jobs**
  * This version has been tested on a media services account with 200 000 assets
  * Some client side queries are disabled with an account with more than 10 000 assets or 5 000 jobs
  * Better performances for jobs and assets delete processes
* More checks (channel and program names, channel properties, Streaming endpoints creation), file overwrite before download
* Bug fixes (channel name sorting, PlayReady relative date,  etc)

Version 3.31.0.0 brings the following features and improvements :

* **New asset download to local** dialog box. The tool can create folders based on the asset name or asset Id and open them when download is completed.
* **Better performance to display assets details** in the grid (cache in memory)
* **Optimization for large number of assets or jobs**.  Search in assets/jobs/channels/programs are now done on all items, not the last 1000 items (queries have been rewritten to be executed by the back-end when possible). This version has been tested on a media services account with 11000 assets. New option to display programs for all channels.
* When playing-back a content, user can select **multiple filters and the no audio-only mode for HLS**, and see the preview of the URL. See the recent [blog post](https://azure.microsoft.com/en-us/blog/azure-media-services-release-dynamic-manifest-composition-remove-hls-audio-only-track-and-hls-i-frame-track-support/) regarding these new features.
* **New software update UI**. Explorer can auto update when a new release is published. Released notes are displayed.
* **Azure Storage settings** dialog box (to activate metrics, and change the default storage in order to allow byte range access for progressive download)
* Option to **Delete all visible assets, or to delete all visible jobs**
* More tasks details in job reports.
* JSON and XML syntax check in Premium Workflow, MES and in multi processors dialog box
* Task option in multiple processors, option to process all visible assets
* Price is displayed for MES jobs
* Live archiving uses now JSON presets
* New updated Media Services documentation (5 CHM files), link to released notes
* Requires .NET 4.6
* Bug fixes

Version 3.30.0.1 brings the following features and improvements :

* **Support for Widevine Modular DRM header insertion** for DASH output with Common Encryption. There is now an option in the tool to add a Widevine header when adding a dynamic encryption policy. A license acquisition URL can be optionally specified (a third party service is needed to deliver the licenses, see this [blog post](https://azure.microsoft.com/en-us/blog/azure-media-services-adds-google-widevine-packaging-for-delivering-multi-drm-stream/)).
* Update to the way Azure Media Player is called for Widevine protected content (protection=widevine or protection=drm)
* New **asset file Edit feature** in asset info/asset files. For example, a manifest or a subtitle file can be directly edited on-line
* Added a button to pass **XML data to Premium Workflow Encoder processor** (to set transcodeSource or setRuntimeProperties data)
* Media Services SDK updated to 3.5.1
* Bug fixes