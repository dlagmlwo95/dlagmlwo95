# Chrome Dev Tools Tricks

```markup
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <title>Document</title>
  </head>
  <body>
    <p onclick="makeGreen()">xBREAKxDOWNx</p>

    <script>
      const dogs = [
        { name: "Snickers", age: 2 },
        { name: "hugo", age: 8 },
      ];

      function makeGreen() {
        const p = document.querySelector("p");
        p.style.color = "#BADA55";
        p.style.fontSize = "50px";
      }

      // Regular(기본)
      console.log("hello");

      // Error
      console.error("Shit!");
      
      //styled(스타일 적용 가능)
      console.log('%c I am some great text', 'font-size:50px;
      backgroound:red;
      text-shadow 10px 10px 0 blue'); 

      // Info
      console.info("Crocodiles eat 3-4 people per year");

      // Testing
      const p = document.querySelector("p");
      console.assert(p.classList.contains("ouch"), "That is wrong!");

      // clearing (클리어)
      console.clear();

      // Viewing DOM Elements
      console.log(p);
      console.dir(p);

      //Grouping together 그룹을 지어서 
      dogs.forEach((dog) => {
        console.groupCollapsed(`${dog.name}`);
        console.log(`This is ${dog.name}`);
        console.log(`${dog.name} is ${dog.age * 7} years old`);
        console.groupEnd(`${dog.name}`);
      });

      //counting
      console.count("wes");
      console.count("wes");
      console.count("wes");
      console.count("Steve");
      console.count("Steve");
      console.count("Steve");
      console.count("wes");
      console.count("Steve");
      console.count("wes");

      //timing 걸린 
      console.time("fetching data");
      fetch("http://api.github.com/users/webos")
        .then((data) => data.json())
        .then((data) => {
          console.timeEnd("fetching data");
          console.log(data);
        });
      console.table(dogs);
    </script>
  </body>
</html>

```

