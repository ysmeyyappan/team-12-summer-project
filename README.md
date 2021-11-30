Img12 =load_img(r’C:\Users\S Thanigai\Dropbox\My PC (DESKTOP-ISATS8C)\Downloads\Face Mask Dataset\withoutmask\356.png’,target_size=(224,224))
Plt.imshow(img12)
Img12 = img_to_array(img12)
Img12 = img12/255.0
Img12 = np.expand_dims(img12,axis=0)
Pred1 = np.argmax(model.predict(img12),axis=1)
If pred1[0] == 0:
    Print(“This image contains mask!!!”)
Else:
    Print(“This image doesn’t contain mask!!!”)
