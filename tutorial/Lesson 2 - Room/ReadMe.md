
Lesson 2 - Room

OK now that we have basic switches working on an image element card, we're going to go to the next step.   Room Lighting.
 
 
To do this, we need a room.
 

1. Download GIMP from gimp.org

2. open the lesson2.psd file in gimp

3. use the lasso tool ![lasso](docs/lasso.png)

4. click on each point to select the outline of the office room.

![office](office.png)


5. copy the room.

6. paste into floating layer, then hit the button to make it into a new layer

![new layer](newlayer.png)


 
7. Click the eye in front of the base layer to hide it so you only see the room shown.

![room](room.png)


8. File > Export As  > office.png   


9. Copy your office.png file to your /www/tutorial folder with your other images.





10.  Download color-lite.card.js from 


11.  Copy the file to your /www/js folder 


12. add the following line to the resources area near the top of your ui-lovelace.yaml

	resources:
	  - url: /local/js/color-lite-card.js
		type: js


		
13. Add the following to your tutorial section near the bottom of your ui-lovelace.yaml
	replace office_light with the name of the light you hooked to that switch. (use the same light or this won't work)


          - type: custom:color-lite-card
            entity: light.office_light
            tap_action:
              action: none    
            image:
              /local/tutorial/office.png   
            style:
              top: 50%
              left: 50%
              width: 100%  		
		