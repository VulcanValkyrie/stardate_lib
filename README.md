# stardate_lib

This is a python3 lib built on top of datetime that does stardates. 

There are a few formats for stardate, only a few of which have specific concrete requirements on how to handle date:
  - The format used in the new movies has been explicitly laid out, and is included in this lib. It consists of:
      - The current year
      - the number of days today is into the year
  - TNG's stardate format is incredibly vague, so I gave it my best shot. Here's what i came up with:  
     -  The first digit is the last digit of the century. This is canon.
     -  The next part, canonically, is the season. Here in the real world, we don't have those, so I just used years since 2000
     -  From here there are 2-3 more digits specified, but they are inconsistent throughout the show as well as being entirely unexplained. In order to fill this slot, I used the number of weeks we are into the year. 
     -The last digit, which is preceded by a decimal point. According to the creators, is a day counter for days in the week.
