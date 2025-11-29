# Ex.No:3(D)    INTERFACE 

## QUESTION:
You are programming bots that analyze weather data. Each bot must implement a common interface and give a prediction.


 Bot Types:

SunBot: Predicts "HOT" if temperature > 30, else "MODERATE".

RainBot: Predicts "COLD" if temperature < 20, else "WARM".

Input:

temperature
botType (1 for SunBot, 2 for RainBot)Output:
Prediction as a string.


<img width="175" height="136" alt="image" src="https://github.com/user-attachments/assets/8c02913d-1144-4376-be82-de6220b99d9d" />


## AIM:
To implement different weather-prediction bots using a common interface and generate predictions based on temperature.


## ALGORITHM :
1.	Read the temperature and bot type from the user.

2. If botType is 1, create a SunBot; otherwise, create a RainBot.

3. Pass the temperature to the selected bot's predict() method.

4. The bot evaluates the temperature and returns the corresponding prediction          string.

5. Output the final prediction.





## PROGRAM:
 ```
/*
Program to implement a Interface using Java
Developed by: SINGAMALA VENKATA SAI KUMAR REDDY
RegisterNumber: 212223230208
*/
```

## SOURCE CODE:

```
import java.util.*;

interface WeatherBot {
    String predict(int temperature);
}

class SunBot implements WeatherBot {
    public String predict(int temperature) {
        if (temperature > 30)
            return "HOT";
        else
            return "MODERATE";
    }
}

class RainBot implements WeatherBot {
    public String predict(int temperature) {
        if (temperature < 20)
            return "COLD";
        else
            return "WARM";
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int temperature = sc.nextInt();
        int botType = sc.nextInt();
        sc.close();

        WeatherBot bot;
        if (botType == 1)
            bot = new SunBot();
        else
            bot = new RainBot();

        System.out.println(bot.predict(temperature));
    }
}
```





## OUTPUT:


<img width="346" height="175" alt="image" src="https://github.com/user-attachments/assets/490649a4-4dd0-429c-9010-1f688154e37c" />


## RESULT:
To implement different weather-prediction bots using a common interface and generate predictions based on temperature.


