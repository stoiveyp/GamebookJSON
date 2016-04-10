# GamebookJSON
Defining a way to store gamebooks in a JSON format, along with clients that use them

## Introduction
I loved "choose your own adventure" books as a child. The fun of finding out if you've made the right choice - keeping your thumb in the previous page just in case. I believe there is still a place for these stories, and for us to create our own, but I think there needs to be a common transferrable format to allow those stories to translate to the modern age. My attempt at this is GamebookJSON.

## Gamebook Format

The primary concern of GamebookJSON is to keep the format simple, allowing a complete story to be easily created and shared. The json format is such that common extensions can be easily added (look at the [Extensions](#extensions) section for any discussed and agreed on)  

The format is currently being defined, and so should be considered v0.1

###Example
```javascript
  {
    "name": "GamebookJSON - The Story"
    "description": "This is the example story made to demonstrate the format of GamebookJSON"
    "author": "A U Thor"
    "startSection":"1"
    "sections":{
      "1": {
        "text": "In your corner of the literary world, there is darkness and chaos. Gamebooks aren't being enjoyed as much as they should have been. You're there, viewing the scene, aware of the potential. What do you do?",
        "choices":[
          {
            "text":"Nothing",
            "moveTo":"2"
          },
          {
            "text":"Spread the GamebookJSON goodness",
            "moveto":"3"
          }
        ]
      },
      "2":{
        "text":"Alone, a single source of light, the darkness is too strong. The stories grow weak, the power of their words lessen until they can cannot sustain you. You take one last look before closing your eyes on their beauty forever."
      },
      "3":{
        "text":"You muster the strength left in the words of the stories around you and announce the start of a change. The flare of interest lightens up your dark corner and others come to investigate, many joining the cause and announcing in turn. You smile, your choice has given the stories you love a chance to be enjoyed once more."
      }
    }
  }
```
### Story Overview
The story is the primary container. As most of the time will be spent within the ``sections`` object the story should be kept light. 

| property | description | required |
| --- | --- | --- |
| name | The story title | yes |
| description | Brief summary of the story | no |
| author | Name of the author | no |
| startsection | The section through which the story starts. This is the first section to render when reading the story, but does not need to be the first section in the ```sections object. | yes |

### Sections
Coming Soon

####Choices
Coming Soon

##Clients
Coming Soon

## Extensions <a name="extensions"></a>
No extensions as of yet - if you have an idea for one, please add it to the issues list for further discussion!
