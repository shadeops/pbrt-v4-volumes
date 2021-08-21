SPP = --spp 4096
GPU = --gpu

all: ./images/aerial_explosion_filmic.png \
	 ./images/teapot_cloud_filmic.png \
	 ./images/ground_explosion_filmic.png \
	 ./images/ground_explosion_alt_filmic.png \
	 ./images/smoke_streams_filmic.png \
	 ./images/matchbulb_filmic.png

./aerial_explosion/aerial_explosion_aces.exr : ./aerial_explosion/aerial_explosion.pbrt
	pbrt $(SPP) $(GPU) --outfile $@ $<

./images/aerial_explosion_filmic.png : ./aerial_explosion/aerial_explosion_aces.exr
	imgtool convert --outfile $@ --colorspace srgb --aces-filmic $<

./teapot_cloud/teapot_cloud_aces.exr : ./teapot_cloud/teapot_cloud.pbrt
	pbrt $(SPP) $(GPU) --outfile $@ $<

./images/teapot_cloud_filmic.png : ./teapot_cloud/teapot_cloud_aces.exr
	imgtool convert --outfile $@ --colorspace srgb --aces-filmic $<

./ground_explosion/ground_explosion_aces.exr : ./ground_explosion/ground_explosion.pbrt
	pbrt $(SPP) $(GPU) --outfile $@ $<

./images/ground_explosion_filmic.png : ./ground_explosion/ground_explosion_aces.exr
	imgtool convert --outfile $@ --colorspace srgb --aces-filmic $<

./ground_explosion/ground_explosion_alt_aces.exr : ./ground_explosion/ground_explosion_alt.pbrt
	pbrt $(SPP) $(GPU) --outfile $@ $<

./images/ground_explosion_alt_filmic.png : ./ground_explosion/ground_explosion_alt_aces.exr
	imgtool convert --outfile $@ --colorspace srgb --aces-filmic $<

./smoke_streams/smoke_streams.exr : ./smoke_streams/smoke_streams.pbrt
	pbrt $(SPP) $(GPU) --outfile $@ $<

./images/smoke_streams_filmic.png : ./smoke_streams/smoke_streams.exr
	imgtool convert --outfile $@ --aces-filmic $<

./matchbulb/matchbulb.exr : ./matchbulb/matchbulb.pbrt
	pbrt $(SPP) $(GPU) --outfile $@ $<

./images/matchbulb_filmic.png : ./matchbulb/matchbulb.exr
	imgtool convert --outfile $@ --aces-filmic $<

clean:
	rm -vf ./images/*.png
	rm -vf */*_aces.exr

