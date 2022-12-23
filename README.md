# pbrt-v4-volumes
A collection of volume renders and their scenes for [pbrt-v4](https://github.com/mmp/pbrt-v4).
* [Ground Explosion](./README.md#ground-explosion)
* [Ground Explosion Alt](./README.md#ground-explosion-alt)
* [Aerial Explosion](./README.md#aerial-explosion)
* [Matchbulb](./README.md#matchbulb)
* [Anemone](./README.md#anemone)
* [Rainbow Box](./README.md#rainbow-box)
* [Smoke Streams](./README.md#smoke-streams)
* [Teapot Cloud](./README.md#teapot-cloud)

To render these you need to use a recent version of pbrt-v4 (specifically https://github.com/mmp/pbrt-v4/tree/06cdbec or newer).

# Examples

### Ground Explosion
![./scenes/images/ground_explosion_filmic.png](/scenes/images/ground_explosion_filmic.png)
```
pbrt --outfile ./ground_explosion/ground_explosion_aces.exr ./ground_explosion/ground_explosion.pbrt
imgtool convert --outfile ./scenes/images/ground_explosion_filmic.png --colorspace srgb --aces-filmic ./ground_explosion/ground_explosion_aces.exr
```

### Ground Explosion Alt
![./scenes/images/ground_explosion_alt_filmic.png](/scenes/images/ground_explosion_alt_filmic.png)
```
pbrt --outfile ./ground_explosion/ground_explosion_alt_aces.exr ./ground_explosion/ground_explosion_alt.pbrt
imgtool convert --outfile ./scenes/images/ground_explosion_alt_filmic.png --colorspace srgb --aces-filmic ./ground_explosion/ground_explosion_alt_aces.exr
```

### Aerial Explosion
![./scenes/images/aerial_explosion_filmic.png](/scenes/images/aerial_explosion_filmic.png)
```
pbrt --outfile ./aerial_explosion/aerial_explosion_aces.exr ./aerial_explosion/aerial_explosion.pbrt
imgtool convert --outfile ./scenes/images/aerial_explosion_filmic.png --colorspace srgb --aces-filmic ./aerial_explosion/aerial_explosion_aces.exr
```

### Matchbulb
![./scenes/images/matchbulb_filmic.png](/scenes/images/matchbulb_filmic.png)
```
pbrt --outfile ./matchbulb/matchbulb.exr ./matchbulb/matchbulb.pbrt
imgtool convert --outfile ./scenes/images/matchbulb_filmic.png --colorspace srgb --aces-filmic ./matchbulb/matchbulb.exr
```

### Anemone
![./scenes/images/anemone_tonemap.png](/scenes/images/anemone_tonemap.png)
```
pbrt --outfile ./anemone/anemone.exr ./anemone/anemone.pbrt
imgtool convert --outfile ./scenes/images/anemone_tonemap.png --colorspace srgb --tonemap ./anemone/anemone.exr
```

### Rainbow Box
![./scenes/images/rainbow_box_tonemap.png](/scenes/images/rainbow_box_tonemap.png)
```
pbrt --outfile ./rainbow_box/rainbow_box.exr ./rainbow_box/rainbow_box.pbrt
imgtool convert --outfile ./scenes/images/rainbow_box_tonemap.png --colorspace srgb --tonemap ./rainbow_box/rainbow_box.exr
```

### Smoke Streams
![./scenes/images/rainbow_box_tonemap.png](/scenes/images/smoke_streams_tonemap.png)
```
pbrt --outfile ./smoke_streams/smoke_streams.exr ./smoke_streams/smoke_streams.pbrt
imgtool convert --outfile ./scenes/images/smoke_streams_tonemap.png --colorspace srgb --tonemap ./smoke_streams/smoke_streams.exr
```

### Teapot Cloud
![./scenes/images/teapot_cloud_filmic.png](/scenes/images/teapot_cloud_filmic.png)
```
pbrt --outfile ./teapot_cloud/teapot_cloud_aces.exr ./teapot_cloud/teapot_cloud.pbrt
imgtool convert --outfile ./scenes/images/teapot_cloud_filmic.png --colorspace srgb --aces-filmic ./teapot_cloud/teapot_cloud_aces.exr
```
