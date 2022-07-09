with the sidebar we use subcomponents to help build it, [[SidebarMenu]], 

using [[heroicons]] for the same icons that the acual website uses quickly and free

```jsx
// heroicons

// import it into the component
import {HomeIcon} from "@heroicons/react/solid";

// apply it to a tag
<SidebarMenu text='Home' Icon={HomeIcon} />
```

Adding the icons as [[props]] to the [[SidebarMenu]] sub-component 

the we use the [[vs code shortcuts]] alt+shift+up/down arrow key to duplicate easily

```jsx
import {HomeIcon} from "@heroicons/react/solid";

<div className="">

        <SidebarMenu text='Home' Icon={HomeIcon} />

        <SidebarMenu text='Home' Icon={HomeIcon} />

        <SidebarMenu text='Home' Icon={HomeIcon} />

        <SidebarMenu text='Home' Icon={HomeIcon} />

        <SidebarMenu text='Home' Icon={HomeIcon} />

        <SidebarMenu text='Home' Icon={HomeIcon} />

        <SidebarMenu text='Home' Icon={HomeIcon} />

      </div>
```

then manually change to this 

```jsx
// import the corresponding packages
import {BellIcon, HashtagIcon, BookmarkIcon, ClipboardIcon, DotsCircleHorizontalIcon, HomeIcon, InboxIcon} from "@heroicons/react/solid";

<div className="">

        <SidebarMenu text='Home' Icon={HomeIcon} />

        <SidebarMenu text='Explore' Icon={HashtagIcon} />

        <SidebarMenu text='Notifications' Icon={BellIcon} />

        <SidebarMenu text='Messages' Icon={InboxIcon} />

        <SidebarMenu text='Bookmarks' Icon={BookmarkIcon} />

        <SidebarMenu text='Lists' Icon={ClipboardIcon} />

        <SidebarMenu text='More' Icon={DotsCircleHorizontalIcon} />

      </div>

```

