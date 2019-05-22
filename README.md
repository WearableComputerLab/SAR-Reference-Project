# SAR-Reference-Project

This is the minimal structure for a Unity project using the SAR Framework. It consists of a single SAR projector and a calibration box at the world origin.

## Screen Adjusted Canvas

To allow for in-editor viewing of a correctly calibrated SAR projector from a single Intrinsic/Extrinsic matrix pair, the SAR projector is configured to use a RenderTexture that matches the screen size used during the calibration. This RenderTexture is then displayed on a fixed pixel canvas and centred on a standard camera. By detaching a game view in the editor and placing it on the projectors desktop view, accurate SAR projections can be viewed without running a standalone build.

The screen adjusted canvas will display correctly on fullscreen standalone builds and can even draw to extra displays by setting the Target Display of the Screen Adjusted Camera.

If you want to render directly to a target display, remember to clear the Target Texture field in the SARProjector component