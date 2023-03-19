## Question.1 => What is an Object In Javascript ?

```
   जावास्क्रिप्ट में ऑब्जेक्ट एक डेटा टाइप होता हैं जिसमें विभिन्न प्रकार के डेटा एवं साथ ही उन्हें एक साथ संगठित किया जाता हैं। ऑब्जेक्ट में वास्तविक डेटा के अलावा फ़ंक्शन एवं विभिन्न मेथड भी होते हैं। ज्यादातर जावास्क्रिप्ट प्रोग्रामिंग में ऑब्जेक्ट बहुत उपयोग में आता है।

            उदाहरण के लिए, एक ऑब्जेक्ट के रूप में एक किताब को संरचित किया जा सकता हैं। किताब में विभिन्न विषयों पर लिखित छोटे छोटे विवरण, कुछ व्याख्यान एवं इनपुट सूचनाएं हो सकती हैं। इसी प्रकार ऑब्जेक्ट में भी विभिन्न टाइप के डेटा हो सकते हैं जैसे कि नंबर, स्ट्रिंग, बूलियन जैसे डेटा टाइप होते हैं।
```

## Question.2 => What Is The Difference Between Dot Noation And Bracket Notation For Accessing Object Propertes ?

```
   डॉट नोटेशन और ब्रैकेट नोटेशन दोनों एक ऑब्जेक्ट की गुणवत्ता तक पहुंच करने के लिए उपयोग किए जाने वाले विभिन्न संकेत हैं। डॉट नोटेशन में, ऑब्जेक्ट की गुणवत्ता नाम के बाद एक डॉट लगाकर लिखी जाती है। जबकि ब्रैकेट नोटेशन में, ऑब्जेक्ट की गुणवत्ता के नाम को ब्रैकेट में लिखा जाता है जो स्ट्रिंग, नंबर या वेरिएबल हो सकता है। जब आप ब्रैकेट नोटेशन का उपयोग करते हैं, तो आप अपनी गुणवत्ता को किसी भी वैल्यू या वेरिएबल से पूर्ण कर सकते हैं। डॉट नोटेशन से इसमें बदलाव नहीं किया जा सकता है क्योंकि यह नाम के साथ सीधे जुड़ा हुआ होता है।
```

## Question.3 => How do you loop through the properties of an object in javascript ?

```
 let obj = { name: "Ashraf", age: 20, city: "Ajmer" };

            for (let key in obj) {
              console.log(key + ": " + obj[key]);
            }
```

## Question.4=> What is the Difference between an object and Array in javascript ?

```
 जावास्क्रिप्ट में ऑब्जेक्ट और एरे दोनों डेटा टाइप होते हैं।

      ऑब्जेक्ट एक संग्रह होता है जो विभिन्न तत्वों को आंकड़ों के रूप में संग्रहित करता है। एक ऑब्जेक्ट की तुलना एक डिक्शनरी से की जा सकती है जहां कुंजी एक वस्तु एवं मूल्य उस वस्तु को उपलब्ध कराता है।

      एरे एक तालिका होती है जो समान या संबंधित मानों के संग्रह को रखती है। एक एरे के साधारण उपयोग हैं डेटा को संग्रहित करने वाले क्षेत्र जो समान प्रकार के होते हैं जैसे संख्याओं की तालिका, स्ट्रिंग की तालिका आदि।
```

## Question.5 => Write a Javascript function to convert an object into a list of `[key,value]` pairs.

```
   function objectToList(obj) {
        return Object.entries(obj);
      }
      const obj = {
        a: 1,
        b: 2,
        c: 3,
      };

      const list = objectToList(obj);
      console.log(list); // [[ 'a', 1 ], [ 'b', 2 ], [ 'c', 3 ]]
```

## Question.6=> write a function that kaes an object representing a person and returns their full name ?

```
    function fullName(person) {
        return person.fristName + " " + person.LastName;
      }

      let person = {
        fristName: "Ashraf",
        LastName: "Khan",
        Age: 20,
        Address: "New District Didwana",
      };
      let ans = fullName(person);
      console.log(ans);
```

## Question.8 => Create an Object With your personal details. Now filter out all the values of the object and show them in descending order

```
 let homes = [
        {
          id: "3",
          Name: "Sajid Ali Khan",
          city: "Jaipur",
          state: "Rajasthan",
          Mobile: 7665121914,
          Address: "HASANPURA",
        },
        {
          id: "4",
          Name: "Mushraf Khan",
          city: "Ajmer",
          state: "Rajasthan",
          Mobile: 7665121914,
          Address: "HASANPURA",
        },
        {
          id: "9",
          Name: "Ashraf Khan",
          city: "Ajmer",
          state: "Rajasthan",
          Mobile: 7665121914,
          Address: "HASANPURA",
        },
        {
          id: "5",
          Name: "Firoj Khan",
          city: "Merta",
          state: "Rajasthan",
          Mobile: 8894131977,
          Address: "Karkwal",
        },
      ];

      homes.sort(function (a, b) {
        return parseFloat(a.id) - parseFloat(b.id);
      });
      homes.sort((a, b) => parseFloat(a.id) - parseFloat(b.id));
      homes.sort((a, b) => parseFloat(b.id) - parseFloat(a.id));
      console.log(homes);

```

## Question.10 => Create a javascript function inside an object which finds max of 3 Numbers Now pr call this function of the object and print the maximum Number

```
    let obj = {
        Name: "Ashraf khan",
        fun: function (a, b, c) {
          if (a > b && a > c) {
            console.log(a);
          } else if (b > a && b > c) {
            console.log(b);
          } else if (c > a && c > b) {
            console.log(c);
          } else {
            console.log("Sorry No Macth");
          }
        },
      };
      let ans = obj.fun(9, 11, 7);
```
