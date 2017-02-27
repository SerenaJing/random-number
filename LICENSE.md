This is a function than can randomly generate integers min to max

        function getRandom(min, max){
          var diff = Math.random() * (max-min);
          var result = Math.round(diff + min);
          result = Math.max(Math.min(result, max), min);
          return result;
        }

But this question is Given a function that randomly generates integers 1 to 5, write a function that randomly generates integers 1 to 7
So I just use this function which from 1 to 5 to generate integers 1 to 7.

      function RandomSeven() {
        var RandomFive = getRandom(1, 5);
        var array = [];
        var result = [];
        var three = [];
        var hash = {};
        var sum = 7;
        var i = 0;
        var temp = 0;
        while(sum--) {
          array.push(RandomFive);
        }
        while(i<7) {
          if(!hash[array[i]]) {
            result.push(srrsy[i]);
            hash[array[i]] = true;
          }
        }
        sum = 3;
        while(sum--) {
          three.push(RandomFive);
        }
        for(i=0;i<3;i++) {
          if(three[i]>three[temp]) {
            temp = i;
          }
        }
        return result[temp];
      }
