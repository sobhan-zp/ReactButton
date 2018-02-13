# ReactButton
Android Library By Java to Create ReactButton with 6 Emoji Face 

Description :

Add ReactButton To Your Current Project :

Add it in your root build.gradle at the end of repositories
    
    allprojects {
        repositories {
			maven { url 'https://jitpack.io' }
		}
	}
    
             
Add the dependency      

    compile 'com.github.AmrDeveloper:ReactButton:1.0.4'
            
Default Case :

    Text = Like 
    Emoji is black Hand
    If User Click on Button it Text Will still like but emoji will be blue hand
    and if user click long on button it will show dialog to choose one emoji from 6 emojis

How To Initializing ReactButton :

```java
ReactButton reactButton = findViewById(R.id.buttonId);
```

Set Emoji Type on Button :

```java
   reactButton.setCurrentEmojiType(String emojiType);
   
   Types : 
   ReactButton.DEFAULT
   ReactButton.LIKE
   ReactButton.LOVE
   ReactButton.SMILE
   ReactButton.WOW
   ReactButton.SAD
   ReactButton.ANGRY
```

To Get Current Emoji On Button :

```java
String currentEmoji = reactButton.getCurrentEmojiType();

switch(currentEmoji)
{
   case ReactButton.LIKE:
       //Text Is Like , Emoji Is Blue Hand
       break;
       
   case ReactButton.LOVE:
       //Text Is Like , Emoji Is Red Heart
       break;
       
   case ReactButton.SMILE:
        //Text Is Smile , Emoji Is Smile Hand
       break;
       
   case ReactButton.WOW:
       //Text Is Wow , Emoji Is Wow Face
       break;
       
   case ReactButton.SAD:
       //Text Is Sad , Emoji Is Dark Hand
       break;
       
   case ReactButton.ANGRY:
       //Text Is Angry , Emoji Is Angry Face
       break; 
       
   default:
       //Text Is Like , Emoji Is Dark Hand
       break;
}
```

Set On Click Listener :

  ```java
  reactButton.setReactClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                //Your Code
            }
   });
   ```

Set on Long Click Listener :

 ```java
  reactButton.setReactDismissListener(new View.OnLongClickListener() {
            @Override
            public boolean onLongClick(View view) {
                //Your Code
                return false;
            }
  });
  ```



