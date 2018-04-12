# Adafruit_RA8875
Adafruit's Arduino driver for the RA8875 TFT driver with BTE Extension


Added some new functions to Display Images from SPI, Moving and Clipping between Layers with BTE.

tft.Transparent_Mode(); 
 
tft.writeTo(LAyer 1 or 2); set Layer!
 
tft.layerEffect(choice) ->LAYER1, LAYER2, TRANSPARENT, LIGHTEN, OR, AND, FLOATING

tft.dispicown(uint16_t x,uint16_t y, uint16_t w,uint16_t h,uint64_t start) Copy SPI to Screen/Selected Layer

tft.layer2_1_transparency(uint8_t setx)


Copy or Clip Layer to Layer
tft.BTE_Move(SourceX, SourceY, Width, Height, DestX, DestY) = copy something visible on the current layer
		
tft.BTE_Move(SourceX, SourceY, Width, Height, DestX, DestY, 2) = copy something from layer 2 to the current layer
		
tft.BTE_Move(SourceX, SourceY, Width, Height, DestX, DestY, 2, 1, true) = copy from layer 2 to layer 1, with the transparency option

tft.BTE_Move(SourceX, SourceY, Width, Height, DestX, DestY, 0, 0, true, RA8875_BTEROP_ADD) = copy on the current layer, using transparency and the ADD/brighter operation 

tft.BTE_Move(SourceX, SourceY, Width, Height, DestX, DestY, 0, 0, false, RA8875_BTEROP_SOURCE, false, true) = copy on the current layer using the reverse direction option for overlapping areas

![Effekts](https://img.youtube.com/vi/3Kj4yj5m_5E/0.jpg)](https://www.youtube.com/watch?v=3Kj4yj5m_5E)  



Look old Version:
https://github.com/schuppeste/RA8875Ada-BTE
