# Molly - A python package for study-booking system of CDUT Library

**This is one of the projects by Twikor. For more, take a step to my blog [Twikor's (twic.me)](https://twic.me).** 

**Molly** is an open source package for python helping handling with the booking process of CDUT Library's study.

## Installation

First, install al the dependencies that are required for this package.
```
pip install terminaltables beautifulsoup4
```
Then clone all the files to your computer(mostly a server for continuous support).

## Structure

**dinner.py** - main library file that contains all the methods that you need to handle the boring works.

**cafe.py** - main application file that is executable to stand by your side whenever you are in need of it.

**kitchens.json** - file containing all the information of the  studies in CDUT library.

**credits.json** - file containing login information

**recipe.json** - the configuration file for automatic study-booking application *cafe.py*

**leftOver.txt** - file recording all the operation

## Usage


Create a filed named **credits.json** besides dinner.py with your login credentials in the following format:

```
{
    "user":"201901010101",
    "passwd":"010101"
}
```

Once the script is imported, it automatically detects the connection to the server. The script will exit automatically if the check fails.

Below is a list of all available methods, help yourself.

### getRoomIdByNumber(roomId)

Return the `roomId` for the specific room with the `roomNumber`.
`roomId` is an int, not a string.

### getRoomNumberById(roomNumber)

Return the `roomNumber` for the specific room with the `roomId`.

### getFreshCookie()

Login to the system using the credentials in credits.json file, and return the fresh cookie.

### getRoomBookingInfo(roomId)

### bookRoom(users = None, roomId = None, beginDay = None, beginTime = None, endDay = None, endTime = None)

```
bookRoom([201906010326,201906010328],97,"2019-10-13","17:02:00","2019-10-13","18:59:59")
```

### renewRoom()

### cancelRoom(bookingId)

Cancel a room with the specific `bookingId` which could be got by using `getMyBookingInfo()` funcion.
Return `True` if successful, or error message if failed.

### getMyBookingInfo(prettified = False)

Refresh the cookie and make the query, then return the booking information of the current user.
Set parameter `prettified` to `True` to use terminal-tables which makes it easier to check the information returnded.

## Contributions guide

TO BE UPDATED
