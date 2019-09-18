# Appium_Scroller
//Scroll in app using appium.
Dimension di = driver.manage().window().getSize();
					int height = di.getHeight();
					int width = di.getWidth();
					TouchAction ts = new TouchAction(driver);
//        	**********************Scroll right to left		*************

					ts.press(PointOption.point((int)(width*0.80),(int)(height/2))).moveTo(PointOption.point((int)(width*0.30),(int)(height/2))).release().perform();
				
//					**********************Scroll left to right	**********************			

					
					ts.press(PointOption.point((int)(width*0.20),(int)(height/2))).moveTo(PointOption.point((int)(width*0.80),(int)(height/2))).release().perform();
//					**********************Scroll up to bottom	********************

					ts.press(PointOption.point((int)(width/2),(int)(height*0.20))).moveTo(PointOption.point((int)(width/2),(int)(height*0.60))).release().perform();

					
//					**********************Scroll bottom to up	  *********************

					ts.press(PointOption.point((int)(width/2),(int)(height*0.70))).moveTo(PointOption.point((int)(width/2),(int)(height*0.20))).release().perform();

					
//			  	****	if you want to stop scrolling at a particular point in other words if you scroll small step by step you can use:*****

					ts.press(PointOption.point((int)(width/2),(int)(height*0.70))).moveTo(PointOption.point((int)(width/2),(int)(height*0.20) )).waitAction(WaitOptions.waitOptions(Duration.ofSeconds(2))).perform();

//			  	**********	and i think you can retrieve useful date from this file..like where to use wait and how to use, where not use release etc..etc..*******
					
