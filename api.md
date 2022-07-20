we use this one for the twitter clone 
- https://saurav.tech/NewsAPI/

we will use next.js's serverSideRendering for this

we also use a [[react hook]] here to show more news articles with every click 

when done the code to do the above between the components looks like this

```jsx

// Widget component

import { SearchIcon } from "@heroicons/react/solid";

import { News } from "./News";

import { useState } from "react";

  

export const Widgets = ({ newsResults }) => {

  const [articleNum, setArticleNum] = useState(3);

  

  return (

    <div className="xl:w-[600px] hidden lg:inline ml-8 space-y-5">

      <div className="w-[90%] xl:w-[75%] sticky top-0 bg-white py-1.5 z-50">

        <div className="flex items-center p-3 rounded-full bg-red-300">

          <SearchIcon className="h-5 z-50 text-gray-500" />

          <input

            className="absolute inset-0 rounded-full pl-11 border-gray-500 text-gray-700 focus:shadow-lg focus:bg-white bg-gray-100 "

            type="text"

            placeholder="Search Twitter"

          />

        </div>

      </div>

  

      <div className="text-gray-700 space-y-3 bg-gray-100 rounded-xl pt-2 w-[90%] xl:w-[75%]">

        <h4 className="font-bold text-xl px-4">Whats happening</h4>

  

        {newsResults.slice(0, articleNum).map((article) => (

          <News key={article.title} article={article} />

        ))}

        <button

          onClick={() => setArticleNum(articleNum + 3)}

          className="text-blue-300 pl-4 pb-3 hover:text-blue-400"

        >

          Show More

        </button>

      </div>

    </div>

  );

};
```

```jsx
export const News = ({ article }) => {

  return (

    <a href={article.url} target="_blank">

      <div className="flex items-center justify-between px-4 py-2 space-x-1 hover:bg-gray-200 transition duration-200 ">

        <div className="space-y-0.5">

          <h6 className="text-sm font-bold ">{article.title}</h6>

          <p className="text-xs font-medium text-gray-500 ">

            {article.source.name}

          </p>

        </div>

        <img

          className="rounded-xl "

          width="70"

          height="70"

          src={article.urlToImage}

          alt="article image"

        />

      </div>

    </a>

  );

};
```






