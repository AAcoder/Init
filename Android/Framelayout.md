Very useful

- Understand it as layers/frames placed over each other 

- Show one of two frames 
There is search box - clicking on it shows Proactive results and typing on it shows Reactive Results. So both of these placed in framelayouy.

Show caption on image. Caption Layer on top of image layer
      <FrameLayout>
             <TextView>
             <ImageView>
       </FrameLayout>

Show  gradient on Image
      <ImageView> background = image.png   src = gradient <ImageView>

      If above not possible (lets say image you are setting it src as you are assigning bitmap to image), then
      <Framelayout>
       <View> background = gradient</View>
       <ImageView> </ImageView>
      </FrameLayout>
 
