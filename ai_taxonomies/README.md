# AI Taxonomies

### AI Capabilities

<!DOCTYPE html>
<head>
  <meta charset="utf-8">
  <title>AI Capabilities</title>
  <link rel="stylesheet" type="text/css" href="assets/linked.css">
  <style>

    /* Testing */
    @import url("assets/imported.css");

    svg {
      border: solid 1px #ddd;
    }

    .internal {
      fill: #f0f;
    }

    #svgs .dependency {
      fill: #f0f;
    }

    svg text {
      text-anchor: right;
      font-size: 16px;
      font-family: Helvetica;
    }

    /* Page Styles */
    body {
      font-family: "Helvetica Neue", Helvetica, Arial;
      width: 1000px;
      margin: 40px auto;
      font-size: 15px;
      line-height: 1.4em;
    }

    h3 {
      font-size: 18px;
      border-top: solid 1px #ddd;
      padding: 20px 0 0 0;
      margin: 20px 0 0 0;
    }

    p {
      color: #333;
    }

    .note {
      color: #999;
    }

    .bookmarklet {
      padding: 3px 8px;
      font-size: 12px;
      font-weight: bold;
      text-decoration: none;
      border-radius: 1em;
      background: #666;
      color: white;
    }

    .bookmarklet.ver2 {
      background: #3FAA90;
    }

    #svgs {
      margin: 20px 0;
    }


    	.node {
    		cursor: pointer;
    	}

    	.node circle {
    	  fill: #fff;
    	  stroke: steelblue;
    	  stroke-width: 1.5px;
    	}

    	.node text {
    	  font: 12px Helvetica;
    	}

    	.link {
  fill: none;
  /*stroke: steelblue;*/
  opacity: 0.3;
  /*stroke-width: 1.5px;*/
}


#levels{
  margin-left: 20px;
}

</style>
</head>

<body>

  <h3>AI Capabilities</h3>
  <div id="svgs"></div>
  <input id="dl"
      name="downloadButton"
      type="button"
      value="Download SVG" />

      <script src="http://d3js.org/d3.v3.min.js"></script>
            <script src="assets/d3-save-svg.min.js"></script>
                  <script type="text/javascript"></script>
<button type="button" onclick="collapseAll()">Collapse All</button>
<button type="button" onclick="expandAll()">Expand All</button>
<div id="viz"></div>
<script>

      var treeData = [
        {
          "name": "Capabilities",
          "parent": "null",
          "size": 101,
          "children": [
            {
              "name": "Perceive",
              "color": "Perceive",
              "size": 25,
              "parent": "Top Level",
              "children": [
                {
                  "name": "Hears",
                  "color": "Perceive",
                  "size": 8,
                  "parent": "Level 2: A",
                  "children": [
                  {
                    "name": "Hears human speech and converts this into text",
                    "color": "Perceive",
                    "size": 5,
                    "parent": "Level 3: A",
                    "children": [
                    {
                      "name": "Hears what the user is saying and converts this into distinct words in order to process the user's request.",
                      "color": "Perceive",
                      "size": 4,
                      "parent": "Level 3: A",
                      "children": [
                      {
                        "name": "Amazon Echo Speech to text",
                        "color": "Perceive",
                        "size": 1,
                        "parent": "Level 4: A",
                      },
                      {
                        "name": "Siri Speech to text",
                        "color": "Perceive",
                        "size": 1,
                        "parent": "Level 4: A",
                      },
                      {
                        "name": "Google Home Speech to text",
                        "color": "Perceive",
                        "size": 1,
                        "parent": "Level 4: A",
                      },
                      {
                        "name": "Bixby Speech to text",
                        "color": "Perceive",
                        "size": 1,
                        "parent": "Level 4: A"
                      }
                      ]
                    },
                    {
                      "name": "Listens to the learner' pronouncing provided text.",
                      "color": "Perceive",
                      "size": 1,
                      "parent": "Level 3: A",
                      "children": [
                      {
                        "name": "Elsa Pronunciation recognition",
                        "color": "Perceive",
                        "size": 1,
                        "parent": "Level 4: A"
                      }
                      ]
                    }

                    ]
                  },
                  {
                    "name": "Hears the sound that speech is coming from and focuses on direction to improve quality of sound input",
                    "color": "Perceive",
                    "size": 1,
                    "parent": "Level 3: A",
                    "children": [
                    {
                      "name": "Hears the direction a sound is coming from. This allows the system to focus; to listen to this direction and ignore sounds coming from the other directions. This results in better speech to text. It also results in higher quality speech when someone is speaking to another person through Echo.",
                      "color": "Perceive",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "Amazon Echo Sound localization",
                        "color": "Perceive",
                        "size": 1,
                        "parent": "Level 5: A"
                      }
                      ]
                    }
                    ]
                  },
                  {
                    "name": "Hears music being played around",
                    "color": "Perceive",
                    "size": 2,
                    "parent": "Level 3: A",
                    "children": [
                    {
                      "name": "Listens to music being played around, which user wants to know what music it is.",
                      "color": "Perceive",
                      "size": 2,
                      "parent": "Level 3: A",
                      "children": [
                      {
                        "name": "Shazam Music recognition",
                        "color": "Perceive",
                        "size": 1,
                        "parent": "Level 5: A"
                      },
                      {
                        "name": "SoundHound Query by humming (QbH)'s Listening",
                        "color": "Perceive",
                        "size": 1,
                        "parent": "Level 5: A"
                      }
                      ]
                    }
                    ]
                  }
                  ]
                },
                {
                  "name": "Reads",
                  "color": "Perceive",
                  "size": 3,
                  "parent": "Level 2: A",
                  "children": [
                  {
                    "name": "Reads text from an image",
                    "color": "Perceive",
                    "size": 3,
                    "parent": "Level 3: A",
                    "children": [
                    {
                      "name": "Reads math problem in an image or on a paper that the camera is capturing.",
                      "color": "Perceive",
                      "size": 2,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "Socratic Text recognition",
                        "color": "Perceive",
                        "size": 1
                      },
                      {
                        "name": "Microsoft Math Solver Problem reading",
                        "color": "Perceive",
                        "size": 1
                      }
                      ]
                    },
                    {
                      "name": "Reads text in whiteboards, documents and business cards using the smartphone camera app.",
                      "color": "Perceive",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "Microsoft Pix Capture Documents reading",
                        "color": "Perceive",
                        "size": 1
                      }
                      ]
                    }
                    ]
                  }
                  ]
                },
                {
                  "name": "Sees",
                  "color": "Perceive",
                  "size": 11,
                  "parent": "Level 2: A",
                  "children": [
                  {
                    "name": "Sees faces in an image",
                    "color": "Perceive",
                    "size": 4,
                    "parent": "Level 3: A",
                    "children": [
                    {
                      "name": "Detects all faces in photos in the user's photo album.",
                      "color": "Perceive",
                      "size": 2,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "Google Photo Face recognition",
                        "color": "Perceive",
                        "size": 1
                      },
                      {
                        "name": "iOS Photo app People",
                        "color": "Perceive",
                        "size": 1
                      }
                      ]
                    },
                    {
                      "name": "Detects a face in a picture that the user took or selected from his/her photo album.",
                      "color": "Perceive",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "FaceApp Face recognition",
                        "color": "Perceive",
                        "size": 1
                      }
                      ]
                    },
                    {
                      "name": "Detects faces in the photo that the user uploaded on Facebook.",
                      "color": "Perceive",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children" : [
                      {
                        "name": "Facebook Face recognition",
                        "color": "Perceive",
                        "size": 1
                      }
                      ]
                    }
                    ]
                  },
                  {
                    "name": "Sees the 3D space the camera is capturing",
                    "color": "Perceive",
                    "size": 2,
                    "parent": "Level 3: A",
                    "children": [
                    {
                      "name": "Recognizes the user's face.",
                      "color": "Perceive",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "iPhone Face ID's Face detection",
                        "color": "Perceive",
                        "size": 1
                      }
                      ]
                    },
                    {
                      "name": "Finds out all present human faces and outputs their bounding box, given an input image or video frame.",
                      "color": "Perceive",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "SnapChat's Face recognition",
                        "color": "Perceive",
                        "size": 1
                      }
                      ]
                    }
                    ]
                  },
                  {
                    "name": "Sees objects in an image",
                    "color": "Perceive",
                    "size": 3,
                    "parent": "Level 3: A",
                    "children": [
                    {
                      "name": "Sees various food in the picture that the user took with the camera or selected from the photo album.",
                      "color": "Perceive",
                      "size": 2,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "Diet Camera AI's Food recognition",
                        "color": "Perceive",
                        "size": 1
                      },
                      {
                        "name": "Calorie Mama's Food recognition",
                        "color": "Perceive",
                        "size": 1
                      }
                      ]
                    },
                    {
                      "name": "Sees tissue growth in a picture of a mole that the user took with his/her smartphone.",
                      "color": "Perceive",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "HealthAI's Mole recognition",
                        "color": "Perceive",
                        "size": 1
                      }
                      ]
                    }
                    ]
                  },
                  {
                    "name": "Sees faces the camera is capturing",
                    "color": "Perceive",
                    "size": 2,
                    "parent": "Level 3: A",
                    "children": [
                    {
                      "name": "Recognizes the user's face.",
                      "color": "Perceive",
                      "size": 1,
                      "parent": "Level 3: A",
                      "children": [
                      {
                        "name": "iPhone Face ID's Face detection",
                        "color": "Perceive",
                        "size": 1
                      }

                      ]
                    },
                    {
                      "name": "Finds out all present human faces and outputs their bounding box, given an input image or video frame.",
                      "color": "Perceive",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "SnapChat's Face recognition",
                        "color": "Perceive",
                        "size": 1
                      }
                      ]
                    }
                    ]
                  }
                  ]
                },
                {
                  "name": "Senses",
                  "color": "Perceive",
                  "size": 3,
                  "parent": "Level 2: A",
                  "children": [
                  {
                    "name": "Senses a user's motion",
                    "color": "Perceive",
                    "size": 1,
                    "parent": "Level 3: A",
                    "children": [
                    {
                      "name": "Senses the user's motion and detects any changes.",
                      "color": "Perceive",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "Apple Watch's Automatic workout detection",
                        "color": "Perceive",
                        "size": 1
                      }
                      ]
                    }
                    ]
                  },
                  {
                    "name": "Senses the surroundings",
                    "color": "Perceive",
                    "size": 2,
                    "parent": "Level 3: A",
                    "children": [
                    {
                      "name": "Perceives its surroundings, combining a variety of sensors such as radar, lidar, sonar, GPS, odometry and inertial measurement units.",
                      "color": "Perceive",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "Waymo's Sensing",
                        "color": "Perceive",
                        "size": 1
                      }
                      ]
                    },
                    {
                      "name": "Perceives its surroundings with multiple sensors.",
                      "color": "Perceive",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "Roomba's Sensing",
                        "color": "Perceive",
                        "size": 1
                      }
                      ]
                    }
                    ]
                  }
                  ]
                }
              ]
            },
            {
              "name": "Evaluate",
              "color": "Evaluate",
              "size": 56,
              "parent": "Top Level",
              "children": [
                {
                  "name": "Recommends from a set",
                  "color": "Evaluate",
                  "size": 29,
                  "parent": "Level 2: A",
                  "children": [
                  {
                    "name": "Recommends products from a set of products",
                    "color": "Evaluate",
                    "size": 1,
                    "parent": "Level 3: A",
                    "children": [
                    {
                      "name": "Recommends new products the user might want to purchase from the set of items Amazon sells with the goal of increasing product sales.",
                      "color": "Evaluate",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "Amazon's Recommender",
                        "color": "Evaluate",
                        "size": 1
                      }
                      ]
                    }
                    ]
                  },
                  {
                    "name": "Recommends codes from a set of codes.",
                    "color": "Evaluate",
                    "size": 2,
                    "parent": "Level 3: A",
                    "children": [
                    {
                      "name": "Suggests the programmer code completions and related content based on the context.",
                      "color": "Evaluate",
                      "size": 2,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "Kite",
                        "color": "Evaluate",
                        "size": 1
                      },
                      {
                        "name": "Codota",
                        "color": "Evaluate",
                        "size": 1
                      }
                      ]
                    }
                    ]
                  },
                  {
                    "name": "Recommends a cover from a set of covers",
                    "color": "Evaluate",
                    "size": 1,
                    "parent": "Level 3: A",
                    "children": [
                    {
                      "name": "Selects and displays a cover graphic for a piece of content based on a small set of possible covers with the goal of making the media more appealing to the user.",
                      "color": "Evaluate",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "Netflix’s Personalized media covers",
                        "color": "Evaluate",
                        "size": 1
                      }
                      ]
                    }
                    ]
                  },
                  {
                    "name": "Recommends a place from a set of housings",
                    "color": "Evaluate",
                    "size": 1,
                    "parent": "Level 3: A",
                    "children": [
                    {
                      "name": "Recommends the places where a user most likely to stay based on the similarities in the places the user clicked on, how long he/she looked at them and the places he/she looked at in the most depth.",
                      "color": "Evaluate",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "Airbnb Recommendations",
                        "color": "Evaluate",
                        "size": 1
                      }
                      ]
                    }
                    ]
                  },
                  {
                    "name": "Recommends hotels from a set of hotels",
                    "color": "Evaluate",
                    "size": 1,
                    "parent": "Level 3: A",
                    "children": [
                    {
                      "name": "Recommends hotels that the user might want to stay from a set of hotels.",
                      "color": "Evaluate",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "Booking.com search results",
                        "color": "Evaluate",
                        "size": 1
                      }
                      ]
                    }
                    ]
                  },
                  {
                    "name": "Recommends a route/transportation from a set of routes/transportations",
                    "color": "Evaluate",
                    "size": 2,
                    "parent": "Level 3: A",
                    "children": [
                    {
                      "name": "Recommends routes and transportations that are most available to the user among the various travel routes/transportations.",
                      "color": "Evaluate",
                      "size": 2,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "Transit",
                        "color": "Evaluate",
                        "size": 1
                      },
                      {
                        "name": "Google Map Directions",
                        "color": "Evaluate",
                        "size": 1
                      }
                      ]
                    }
                    ]
                  },
                  {
                    "name": "Recommends a taxi from a set of taxis",
                    "color": "Evaluate",
                    "size": 1,
                    "parent": "Level 3: A",
                    "children": [
                    {
                      "name": "Connects the passenger with the best taxi driver, among other taxi drivers, to take him or her to the destination.",
                      "color": "Evaluate",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "Uber Passenger/driver matching",
                        "color": "Evaluate",
                        "size": 1
                      }
                      ]
                    }
                    ]
                  },
                  {
                    "name": "Recommends apps from a set of apps.",
                    "color": "Evaluate",
                    "size": 1,
                    "parent": "Level 3: A",
                    "children": [
                    {
                      "name": "Makes suggestions for what the user might want to do next at just the right time based on his/her routines and how he/she use apps.",
                      "color": "Evaluate",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "iOS App suggestion",
                        "color": "Evaluate",
                        "size": 1
                      }
                      ]
                    }
                    ]
                  },
                  {
                    "name": "Recommends music from a set of music.",
                    "color": "Evaluate",
                    "size": 3,
                    "parent": "Level 3: A",
                    "children": [
                    {
                      "name": "Provides a user with a personalized playlist that the user is expected to enjoy listening to.",
                      "color": "Evaluate",
                      "size": 3,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "Spotify Discover Weekly",
                        "color": "Evaluate",
                        "size": 1
                      },
                      {
                        "name": "Pandora's Music recommendation",
                        "color": "Evaluate",
                        "size": 1,
                      },
                      {
                        "name": "Apple Music Recommender",
                        "color": "Evaluate",
                        "size": 1
                      }
                      ]
                    }
                    ]
                  },
                  {
                    "name": "Recommends photos from a set of photos",
                    "color": "Evaluate",
                    "size": 1,
                    "parent": "Level 3: A",
                    "children": [
                    {
                      "name": "Recommends the user photos and videos he/she most likely wants to see.",
                      "color": "Evaluate",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "Instagram’s Search suggestion",
                        "color": "Evaluate",
                        "size": 1
                      }
                      ]
                    }
                    ]
                  },
                  {
                    "name": "Recommends pins from a set of pins",
                    "color": "Evaluate",
                    "size": 1,
                    "parent": "Level 3: A",
                    "children": [
                    {
                      "name": "Recommends relevant content that meets users' search results and interests. It ranks and prioritizes pins based on their quality, and presents a series of more accurate images, in which users can then click on to access their desired content.",
                      "color": "Evaluate",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "Pinterest Home feed",
                        "color": "Evaluate",
                        "size": 1
                      }
                      ]
                    }
                    ]
                  },
                  {
                    "name": "Recommends posts from a set of posts.",
                    "color": "Evaluate",
                    "size": 3,
                    "parent": "Level 3: A",
                    "children": [
                    {
                      "name": "Recommends jobs, topics, or connections that a user might be interested in to build his/her career, and recommends posts related to them.",
                      "color": "Evaluate",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "LinkedIn Home feed",
                        "color": "Evaluate",
                        "size": 1
                      }
                      ]
                    },
                    {
                      "name": "Recommends content posted from friends over publishers, with a focus on meaningful interactions.",
                      "color": "Evaluate",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "Facebook NewsFeed",
                        "color": "Evaluate",
                        "size": 1
                      }
                      ]
                    },
                    {
                      "name": "Shows tweets from accounts the user follows by ranking signals. In addition to ranked content from followers, this feed will sometimes feature who to follow suggests, and content from other accounts.",
                      "color": "Evaluate",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "Twitter Home feed",
                        "color": "Evaluate",
                        "size": 1
                      }
                      ]
                    }
                    ]
                  },
                  {
                    "name": "Recommends restaurants from a set of restaurants",
                    "color": "Evaluate",
                    "size": 3,
                    "parent": "Level 3: A",
                    "children": [
                    {
                      "name": "Recommends restaurants that the user might visit from the restaurants in the Yelp's database.",
                      "color": "Evaluate",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "Yelp's Recommender",
                        "color": "Evaluate",
                        "size": 1
                      }
                      ]
                    },
                    {
                      "name": "Recommends restaurants that the user might visit soon from a set of restaurants in the OpenTable's database.",
                      "color": "Evaluate",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "Open Table Restaurants List",
                        "color": "Evaluate",
                        "size": 1
                      }
                      ]
                    },
                    {
                      "name": "Recommends restaurants that the user might want to order food soon from a set of restaurants.",
                      "color": "Evaluate",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "Grubhub Restaurants list",
                        "color": "Evaluate",
                        "size": 1
                      }
                      ]
                    }
                    ]
                  },
                  {
                    "name": "Recommends user profiles from a set of other users",
                    "color": "Evaluate",
                    "size": 2,
                    "parent": "Level 3: A",
                    "children": [
                    {
                      "name": "Recommends user profiles that the user might date with from users of Tinder.",
                      "parent": "Level 4: A",
                      "color": "Evaluate",
                      "size": 1,
                      "children": [
                      {
                        "name": "Tinder profile suggestions",
                        "color": "Evaluate",
                        "size": 1
                      }
                      ]
                    },
                    {
                      "name": "Recommends user profiles that the user might want to make a friend from users of Bumble bff.",
                      "color": "Evaluate",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "Bumble bff friends suggestions",
                        "color": "Evaluate",
                        "size": 1
                      }
                      ]
                    }
                    ]
                  },
                  {
                    "name": "Recommends news articles from a set of articles",
                    "color": "Evaluate",
                    "size": 1,
                    "parent": "Level 3: A",
                    "children": [
                    {
                      "name": "Recommends news articles that the user might want to read from a set of articles in the New York Times",
                      "color": "Evaluate",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "New York Times For You",
                        "color": "Evaluate",
                        "size": 1
                      }
                      ]
                    }
                    ]
                  },
                  {
                    "name": "Recommends videos from a set of videos.",
                    "color": "Evaluate",
                    "size": 4,
                    "parent": "Level 3: A",
                    "children": [
                    {
                      "name": "Surfaces videos that a wide range of viewers would find interesting, like a new song from a popular artist or a new movie trailer and a viral video.",
                      "parent": "Level 4: A",
                      "color": "Evaluate",
                      "size": 1,
                      "children": [
                      {
                        "name": "YouTube Trending",
                        "color": "Evaluate",
                        "size": 1
                      }
                      ]
                    },
                    {
                      "name": "Recommends a show or movie from a variety set of contents to users.",
                      "color": "Evaluate",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "Prime Video Recommendation",
                        "color": "Evaluate",
                        "size": 1
                      }
                      ]
                    },
                    {
                      "name": "Selects and displays short videos that the user will like most, among a variety set of them.",
                      "color": "Evaluate",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "TikTok Video feed",
                        "color": "Evaluate",
                        "size": 1
                      }
                      ]
                    },
                    {
                      "name": "Recommends video content that a user would like to see and continuously presents videos similar to the content that the user watched.",
                      "color": "Evaluate",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "Facebook Watch",
                        "color": "Evaluate",
                        "size": 1
                      }
                      ]
                    }
                    ]
                  },
                  {
                    "name": "Recoomends files from a set of files.",
                    "color": "Evaluate",
                    "size": 1,
                    "parent": "Level 3: A",
                    "children": [
                    {
                      "name": "Suggests files that the user most likely to be interested in working on in a given moment considering recency, frequency, collaborators, and more.",
                      "color": "Evaluate",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "Google Drive's Priority",
                        "color": "Evaluate",
                        "size": 1
                      }
                      ]
                    }
                    ]
                  }

                  ]
                },
                {
                  "name": "Classifies items",
                  "color": "Evaluate",
                  "size": 5,
                  "parent": "Level 2: A",
                  "children": [
                  {
                    "name": "Classifies images by certain criteria.",
                    "color": "Evaluate",
                    "size": 3,
                    "parent": "Level 3: A",
                    "children": [
                    {
                      "name": "Classfies photos by people it detected from the user's photo album.",
                      "color": "Evaluate",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "Google Photo Person classification",
                        "color": "Evaluate",
                        "size": 1
                      }
                      ]
                    },
                    {
                      "name": "Analyzes the images in the user's photo album and classifies them into necessary and unnecessary ones.",
                      "color": "Evaluate",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "Google Photo Clear the clutter",
                        "color": "Evaluate",
                        "size": 1
                      }
                      ]
                    },
                    {
                      "name": "Finds the pictures it thinks are junk, leaving the photos users actually care about. (Users can review the automatically-generated results before they delete them to make sure nothing important gets destroyed.)",
                      "color": "Evaluate",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "Siftr Magic Cleaner",
                        "color": "Evaluate",
                        "size": 1
                      }
                      ]
                    }
                    ]
                  },
                  {
                    "name": "Classifies email as spam and not spam.",
                    "color": "Evaluate",
                    "size": 2,
                    "parent": "Level 3: A",
                    "children": [
                    {
                      "name": "Classifies emails in the user's email inbox into spam and not.",
                      "color": "Evaluate",
                      "size": 2,
                      "parent": "Levle 4: A",
                      "children": [
                      {
                        "name": "Mac OS Email App Spam filtering",
                        "color": "Evaluate",
                        "size": 1
                      },
                      {
                        "name": "Gmail App Spam filtering",
                        "color": "Evaluate",
                        "size": 1
                      }
                      ]
                    }
                    ]
                  }

                  ]
                },
                {
                  "name": "Identifies the user's status",
                  "color": "Evaluate",
                  "size": 2,
                  "parent": "Level 2: A",
                  "children": [
                  {
                    "name": "Identifies a user's motion",
                    "color": "Evaluate",
                    "size": 1,
                    "parent": "Level 3: A",
                    "children": [
                    {
                      "name": "Identifies what the user's motion is, such as walking or running.",
                      "color": "Evaluate",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "Apple Watch's Automatic workout Identification",
                        "color": "Evaluate",
                        "size": 1
                      }
                      ]
                    }
                    ]
                  },
                  {
                    "name": "Identifies symptoms that are generally associated with risky moles.",
                    "color": "Evaluate",
                    "size": 1,
                    "parent": "Level 3: A",
                    "children": [
                    {
                      "name": "IdIdentifies symptoms that are generally associated with risky moles that it sees.",
                      "color": "Evaluate",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "HealthAI's Diagnosis",
                        "color": "Evaluate",
                        "size": 1
                      }
                      ]
                    }
                    ]
                  }
                  ]
                },
                {
                  "name": "Finds wrong parts",
                  "color": "Evaluate",
                  "size": 2,
                  "parent": "Level 2: A",
                  "children": [
                  {
                    "name": "Finds if the wong part from the text the user has entered.",
                    "color": "Evaluate",
                    "size": 1,
                    "parent": "Level 3: A",
                    "children": [
                    {
                      "name": "Analyzes text the user entered and identifies spelling mistakes, grammatical errors, awkward expressions, etc., and recommends appropriate alternatives.",
                      "color": "Evaluate",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "Grammarly’s Auto-correction",
                        "color": "Evaluate",
                        "size": 1
                      }
                      ]
                    }
                    ]
                  },
                  {
                    "name": "Finds the wrong parts from what the user has pronounced.",
                    "color": "Evaluate",
                    "size": 1,
                    "parent": "Level 3: A",
                    "children": [
                    {
                      "name": "Matches up what the user said with the correct American English pronounciation and makes suggestions as to how the speaker can improve on a given sound – for example, by telling them how to shape their mouth or move their tongue.",
                      "color": "Evaluate",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "Elsa Pronunciation correction",
                        "color": "Evaluate",
                        "size": 1
                      }
                      ]
                    }
                    ]
                  }
                  ]
                },
                {
                  "name": "Identifies who the person is",
                  "color": "Evaluate",
                  "size": 3,
                  "parent": "Level 2: A",
                  "children": [
                  {
                    "name": "Determines if the detected face is authorized.",
                    "color": "Evaluate",
                    "size": 1,
                    "parent": "Level 3: A",
                    "children": [
                    {
                      "name": "Determines whether the recognized face is the face of the user of the device.",
                      "color": "Evaluate",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "iPhone Face ID's Person identification",
                        "color": "Evaluate",
                        "size": 1
                      }
                      ]
                    }
                    ]

                  },
                  {
                    "name": "Identifies individual voice of each user.",
                    "color": "Evaluate",
                    "size": 1,
                    "parent": "Level 3: A",
                    "children": [
                    {
                      "name": "Identifies individual voices for a more personalized music experience on HomePod.",
                      "color": "Evaluate",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "Siri HomePod Voice recognition",
                        "color": "Evaluate",
                        "size": 1
                      }
                      ]
                    }
                    ]

                  },
                  {
                    "name": "Finds whose face is detected based on the set of friends.",
                    "color": "Evaluate",
                    "size": 1,
                    "parent": "Level 3: A",
                    "children": [
                    {
                      "name": "Finds whose face is detected based on the set of friends the user has",
                      "color": "Evaluate",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "Facebook Friends Tagging",
                        "color": "Evaluate",
                        "size": 1
                      }
                      ]
                    }
                    ]

                  }
                  ]
                },
                {
                  "name": "Groups objects by subject",
                  "color": "Evaluate",
                  "size": 1,
                  "parent": "Level 2: A",
                  "children": [
                  {
                    "name": "Groups photos by theme and recommends it to the user.",
                    "color": "Evaluate",
                    "size": 1,
                    "parent": "Level 3: A",
                    "children": [
                    {
                      "name": "Groups photos and videos into topics that a user would like to see, and presents them to the user.",
                      "color": "Evaluate",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "iOS Photo app Memories",
                        "color": "Evaluate",
                        "size": 1
                      }
                      ]

                    }
                    ]
                  }
                  ]
                },
                {
                  "name": "Finds out what the object is",
                  "color": "Evaluate",
                  "size": 6,
                  "parent": "Level 2: A",
                  "children": [
                  {
                    "name": "Finds out what kinds of food from various foods.",
                    "color": "Evaluate",
                    "size": 2,
                    "parent": "Level 3: A",
                    "children": [
                    {
                      "name": "Finds out what kind of food they are among various foods, and counts their calories.",
                      "parent": "Level 4: A",
                      "color": "Evaluate",
                      "size": 2,
                      "children": [
                      {
                        "name": "Diet Camera AI's Food identification",
                        "color": "Evaluate",
                        "size": 1
                      },
                      {
                        "name": "Calorie Mama's Food identification",
                        "color": "Evaluate",
                        "size": 1
                      }
                      ]
                    }
                    ]
                  },
                  {
                    "name": "Finds out what music it is.",
                    "color": "Evaluate",
                    "size": 2,
                    "parent": "Level 3: A",
                    "children": [
                    {
                      "name": "Identifies songs in just a few seconds. It matches a song to a massive library of music, and presents the matched song to users.",
                      "color": "Evaluate",
                      "size": 2,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "Shazam Music finder",
                        "color": "Evaluate",
                        "size": 1
                      },
                      {
                        "name": "SoundHound Query by humming (QbH) Music identification",
                        "color": "Evaluate",
                        "size": 1
                      }
                      ]
                    }
                    ]
                  },
                  {
                    "name": "Finds out what the problem is.",
                    "color": "Evaluate",
                    "size": 2,
                    "parent": "Level 3: A",
                    "children": [
                    {
                      "name": "Finds the type of math problem based on a set of possible math problem types.",
                      "color": "Evaluate",
                      "size": 2,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "Socratic's Problem solving",
                        "color": "Evaluate",
                        "size": 1
                      },
                      {
                        "name": "Microsoft Math Solver's Solution suggestion",
                        "color": "Evaluate",
                        "size": 1
                      }
                      ]
                    }
                    ]
                  }
                  ]

                },
                {
                  "name": "Finds imporatant information",
                  "color": "Evaluate",
                  "size": 3,
                  "parent": "Level 2: A",
                  "children": [
                  {
                    "name": "Finds meaningful relationships between information users entered",
                    "color": "Evaluate",
                    "size": 1,
                    "parent": "Level 3: A",
                    "children": [
                    {
                      "name": "Analyzes the information the user entered and finds meaningful relationships between it and what other users have entered.",
                      "color": "Evaluate",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "ResearchGate Confirmation",
                        "color": "Evaluate",
                        "size": 1
                      }
                      ]
                    }
                    ]

                  },
                  {
                    "name": "Finds the text related to an event.",
                    "color": "Evaluate",
                    "size": 2,
                    "parent": "Level 3: A",
                    "children": [
                    {
                      "name": "Finds information related to a specific place or time in the text of emails.",
                      "color": "Evaluate",
                      "size": 2,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "Mac OS Email App Entity recognition",
                        "color": "Evaluate",
                        "size": 1
                      },
                      {
                        "name": "iOS Email App Entity recognition ",
                        "color": "Evaluate",
                        "size": 1
                      }
                      ]
                    }
                    ]

                  }
                  ]
                },
                {
                  "name": "Finds information the user needs",
                  "color": "Evaluate",
                  "size": 5,
                  "parent": "Level 2: A",
                  "children": [
                  {
                    "name": "Finds appropriate information for the user's request",
                    "color": "Evaluate",
                    "size": 2,
                    "parent": "Level 3: A",
                    "children": [
                    {
                      "name": "Finds and provides the most appropriate information for the user's request or question.",
                      "color": "Evaluate",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "Siri Search results",
                        "color": "Evaluate",
                        "size": 1
                      }
                      ]
                    },
                    {
                      "name": "Finds web pages that are related to the query the user entered.",
                      "color": "Evaluate",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "Google Search results",
                        "color": "Evaluate",
                        "size": 1
                      }
                      ]
                    }
                    ]
                  },
                  {
                    "name": "Finds appropriate information to help the user's mental health.",
                    "color": "Evaluate",
                    "size": 3,
                    "parent": "Level 3: A",
                    "children": [
                    {
                      "name": "Identifies a user's emotional state based on text the user entered or options on questions, and provides him/her with the appropriate information, and helps to keep his/her mental health stable.",
                      "color": "Evaluate",
                      "size": 3,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "Uni Magic AI Friend",
                        "color": "Evaluate",
                        "size": 1
                      },
                      {
                        "name": "Woebot",
                        "color": "Evaluate",
                        "size": 1
                      },
                      {
                        "name": "Wysa",
                        "color": "Evaluate",
                        "size": 1
                      }
                      ]
                    }
                    ]
                  }
                  ]
                }
              ]
            },
            {
              "name": "Predict",
              "color": "Predict",
              "size": 18,
              "parent": "Top Level",
              "children": [
                {
                  "name": "Predicts how objects change",
                  "color": "Predict",
                  "size": 3,
                  "parent": "Level 2: A",
                  "children": [
                  {
                    "name": "Predicts how the image changes when each option is applied.",
                    "color": "Predict",
                    "size": 3,
                    "parent": "Level 3: A",
                    "children": [
                    {
                      "name": "Shows how the detected face in the image changes when each option(filter) is applied.",
                      "color": "Predict",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "FaceApp Face transformation",
                        "color": "Predict",
                        "size": 1
                      }
                      ]
                    },
                    {
                      "name": "Transforms photographs into the various styles of painting.",
                      "color": "Predict",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "Prisma's Transforming photos into paintings",
                        "color": "Predict",
                        "size": 1
                      }
                      ]
                    },
                    {
                      "name": "Distorts certain areas of the provided face by enhancing them or adding something on top of them with various filters and options.",
                      "color": "Predict",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "SnapChat's Face filter",
                        "color": "Predict",
                        "size": 1
                      }
                      ]
                    }
                    ]
                  }
                  ]
                },
                {
                  "name": "Predicts the user's next behavior",
                  "color": "Predict",
                  "size": 3,
                  "parent": "Level 2: A",
                  "children": [
                  {
                    "name": "Predicts what a user is going to type.",
                    "color": "Predict",
                    "size": 2,
                    "parent": "Level 3: A",
                    "children": [
                    {
                      "name": "Predicts and suggests the rest of the text the user is writing so that the user can complete his/her email more quickly.",
                      "color": "Predict",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "G-mail Auto complete",
                        "color": "Predict",
                        "size": 1
                      }
                      ]
                    },
                    {
                      "name": "Provides the user with helpful predictions when he/she enters text with the keyboard so its users can get their points across fast.",
                      "color": "Predict",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "SwiftKey Keyboard Text prediction",
                        "color": "Predict",
                        "size": 1
                      }
                      ]
                    }
                    ]

                  },
                  {
                    "name": "Predicts the user's behavior based on the user's routine.",
                    "color": "Predict",
                    "size": 1,
                    "parent": "Level 3: A",
                    "children": [
                    {
                      "name": "Predicts and suggests the user's behavior such as ordering coffee via a cafe app based on the user's routine and suggests shorcuts.",
                      "color": "Predict",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "Siri Shortcuts suggestion",
                        "color": "Predict",
                        "size": 1
                      }
                      ]
                    }
                    ]

                  }
                  ]
                },
                {
                  "name": "Predicts optimal value",
                  "color": "Predict",
                  "size": 3,
                  "parent": "Level 2: A",
                  "children": [
                  {
                    "name": "Predicts the estimated time.",
                    "color": "Predict",
                    "size": 1,
                    "parent": "Level 3: A",
                    "children": [
                    {
                      "name": "Estimates how soon a user could get the destination as well as how the price will be",
                      "parent": "Level 4: A",
                      "color": "Predict",
                      "size": 1,
                      "children": [
                      {
                        "name": "Uber Time of arrival",
                        "color": "Predict",
                        "size": 1
                      }
                      ]
                    }
                    ]
                  },
                  {
                    "name": "Predicts how long a user's travel will take.",
                    "color": "Predict",
                    "size": 1,
                    "parent": "Level 3: A",
                    "children": [
                    {
                      "name": "Predicts more accurate travel times based on live traffic conditions along users' route, allowing users to see if a bus will be late or how long the delay will be.",
                      "color": "Predict",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "Google Map Bus delay prediction",
                        "color": "Predict",
                        "size": 1
                      }
                      ]
                    }
                    ]
                  },
                  {
                    "name": "Predicts optimal room temperature.",
                    "color": "Predict",
                    "size": 1,
                    "parent": "Level 3: A",
                    "children": [
                    {
                      "name": "Analyzes the user's history and calculates the optimal temperature at each time.",
                      "color": "Predict",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "Nest Learning Thermostat",
                        "color": "Predict",
                        "size": 1
                      }
                      ]
                    }
                    ]
                  }
                  ]
                },
                {
                  "name": "Predicts how text changes",
                  "color": "Predict",
                  "size": 3,
                  "parent": "Level 2: A",
                  "children": [
                  {
                    "name": "Predicts how the text will be translated into other languages.",
                    "color": "Predict",
                    "size": 3,
                    "parent": "Level 3: A",
                    "children": [
                    {
                      "name": "Translates text the camera is capturing into another language in real-time.",
                      "color": "Predict",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "Google Lens (Search) Translation",
                        "color": "Predict",
                        "size": 1
                      }
                      ]

                    },
                    {
                      "name": "Translate the text the user entered into a language different from the original language.",
                      "color": "Predict",
                      "size": 2,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "PapaGo Translate",
                        "color": "Predict",
                        "size": 1
                      },
                      {
                        "name": "Google Translate",
                        "color": "Predict",
                        "size": 1
                      }
                      ]

                    }
                    ]
                  }
                  ]
                },
                {
                  "name": "Simulates",
                  "color": "Predict",
                  "size": 6,
                  "parent": "Level 2: A",
                  "children": [
                  {
                    "name": "Simulates how space will look when the object is placed.",
                    "color": "Predict",
                    "size": 5,
                    "parent": "Level 3: A",
                    "children": [
                    {
                      "name": "Simulates an object in the real world by putting an animated object in real-world space with 3D augmented reality models.",
                      "color": "Predict",
                      "size": 5,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "Angry Birds AR's 3D object",
                        "color": "Predict",
                        "size": 1
                      },
                      {
                        "name": "Amazon AR's 3D object",
                        "color": "Predict",
                        "size": 1
                      },
                      {
                        "name": "IKEA Place's 3D object",
                        "color": "Predict",
                        "size": 1
                      },
                      {
                        "name": "Wayfair View in Room 3D object simulation",
                        "color": "Predict",
                        "size": 1
                      },
                      {
                        "name": "Google AR Search 3D object",
                        "color": "Predict",
                        "size": 1
                      }
                      ]
                    }
                    ]
                  },
                  {
                    "name": "Predicts what it would look like if it were a flat document that was recognized in the image.",
                    "color": "Predict",
                    "size": 1,
                    "parent": "Level 3: A",
                    "children": [
                    {
                      "name": "Transforns the objects in the image in a straight-on perspective, by improving the image, such as cropping edges, boosting color and tone, sharpening focus.",
                      "color": "Predict",
                      "size": 1,
                      "parent": "Level 4: A",
                      "children": [
                      {
                        "name": "Microsoft Pix Capture Documents text extraction",
                        "color": "Predict",
                        "size": 1
                      }
                      ]
                    }
                    ]
                  }
                  ]
                }
              ]
            },
            {
              "name": "Act",
              "color": "Act",
              "size": 2,
              "parent": "Top Level",
              "children": [
                {
                  "name": "Learns the surroundings and adjusts to it in real time",
                  "color": "Act",
                  "size": 2,
                  "parent": "Level 2: A",
                  "children": [
                  {
                    "name": "Analyzes a variety of surrounding information in real time and adjusts the optimal movement for it.",
                    "color": "Act",
                    "size": 2,
                    "parent": "Level 2: A",
                    "children": [
                    {
                      "name": "Analyzes the information collected from the surrounding environment – traffic conditions, obstacles, signs – in real time, and responds to them appropriately, and autonomously drives.",
                      "color": "Act",
                      "size": 1,
                      "parent": "Level 2: A",
                      "children": [
                      {
                        "name": "Waymo's Auto-driving",
                        "color": "Act",
                        "size": 1,
                        "parent": "Level 2: A"
                      }
                      ]
                    },
                    {
                      "name": "Interprets sensory information to identify appropriate navigation paths, as well as obstacles and dusty spots.",
                      "color": "Act",
                      "size": 1,
                      "parent": "Level 2: A",
                      "children": [
                      {
                        "name": "Roomba's Auto-driving",
                        "color": "Act",
                        "size": 1,
                        "parent": "Level 2: A"
                      }
                      ]
                    }
                    ]
                  }
                  ]
                }
              ]

            }


          ]
        }
      ];


      // ************** Generate the tree diagram	 *****************
      var margin = {top: 120, right:500, bottom: 120, left: 700},
      	width = 4000 - margin.right - margin.left,
      	height = 6400 - margin.top - margin.bottom;

      var i = 0,
      	duration = 750,
      	root;

      var tree = d3.layout.tree()
      	.size([height, width]);

        var edge_weight = d3.scale.linear()
        					.domain([0, 100])
                            .range([0, 100]);



      var diagonal = d3.svg.diagonal()
      	.projection(function(d) { return [d.y, d.x]; });

      var svg = d3.select("body").append("svg")
      	.attr("width", width + margin.right + margin.left)
      	.attr("height", height + margin.top + margin.bottom)
        .append("g")
      	.attr("transform", "translate(" + margin.left + "," + margin.top + ")");


      root = treeData[0];
      root.x0 = height / 2;
      root.y0 = 0;
      root.children.forEach(collapse);
      update(root);

      d3.select(self.frameElement).style("height", "800px");

      function update(source) {

        // Compute the new tree layout.
        var nodes = tree.nodes(root).reverse(),
            links = tree.links(nodes);

        // Normalize for fixed-depth.
  nodes.forEach(function(d) { d.y = d.depth * 500; });

        // Update the nodes…
        var node = svg.selectAll("g.node")
            .data(nodes, function(d) { return d.id || (d.id = ++i); });

        // Enter any new nodes at the parent's previous position.
        var nodeEnter = node.enter().append("g")
            .attr("class", "node")
            .attr("transform", function(d) { return "translate(" + source.y0 + "," + source.x0 + ")"; })
            .on("click", click);

            nodeEnter.append("circle")
                .attr("r", 1e-6)
                .style("fill", function(d) { return d._children ? "lightsteelblue" : "#fff"; });

          nodeEnter.append('text')
              .attr('x', function (d) {
                  return d.children || d._children ? -13 : 13;
              })
              .attr('dy', '.35em')
              .attr('text-anchor', function (d) {
                  return d.children || d._children ? 'end' : 'start';
              })
              .text(function (d) {
                  return d.name;
              })
              .call(wrap, 400)
              .style('fill-opacitsy', 1e-6);


              var nodeUpdate = node.transition()
                  .duration(duration)
                  .attr("transform", function(d) { return "translate(" + d.y + "," + d.x + ")"; });

              nodeUpdate.select("circle")
                  .attr("r", function(d){ return edge_weight(d.size/2);})
                  .style("fill", function(d) {
                  return d._children ? "lightsteelblue" : "#fff"; });

              nodeUpdate.select("text")
                  .style("fill-opacity", 1)
                  .style("font-size", function(d){return edge_weight(d.size/2+13)});


        // Transition exiting nodes to the parent's new position.
        var nodeExit = node.exit().transition()
            .duration(duration)
            .attr("transform", function(d) { return "translate(" + source.y + "," + source.x + ")"; })
            .remove();

            nodeExit.select("circle")
                .attr("r", 1e-6);

            nodeExit.select("text")
                .style("fill-opacity", 1e-6);

            // Update the linksâ€¦
            var link = svg.selectAll("path.link")
                .data(links, function(d) { return d.target.id; });


        // Enter any new links at the parent's previous position.
        link.enter().insert("path", "g")
            .attr("class", "link")
            .attr("stroke-width", function(d){
            	return 1;
            })
            .attr("d", function(d) {
              var o = {x: source.x0, y: source.y0};
              return diagonal({source: o, target: o});
            })
            .attr("stroke", function(d){
            	return linkColor(d.target.color);});


              // Transition links to their new position.
              link.transition()
                  .duration(duration)
                  .attr("d", function(d){
                  /* calculating the top shift */
                  var source = {x: d.source.x - edge_weight(calculateLinkSourcePosition(d)), y: d.source.y};
                  var target = {x: d.target.x, y: d.target.y};
                  return diagonal({source: source, target: target});
                  })
                  .attr("stroke-width", function(d){
                  	return edge_weight(d.target.size);
                  });

              // Transition exiting nodes to the parent's new position.
              link.exit().transition()
                  .duration(duration)
                  .attr("d", function(d) {
                    var o = {x: source.x, y: source.y};
                    return diagonal({source: o, target: o});
                  })
                  .remove();

              // Stash the old positions for transition.
              nodes.forEach(function(d) {
                d.x0 = d.x;
                d.y0 = d.y;
              });
            }

            function calculateLinkSourcePosition(link) {
            	targetID = link.target.id;
            	var childrenNumber = link.source.children.length;
            	var widthAbove = 0;
            	for (var i = 0; i < childrenNumber; i++)
            	{
            		if (link.source.children[i].id == targetID)
            		{
            			// we are done
            			widthAbove = widthAbove + link.source.children[i].size/2;
            			break;
            		}else {
            			// keep adding
            			widthAbove = widthAbove + link.source.children[i].size
            		}
            	}
            	return link.source.size/2 - widthAbove;
            }


            /*
             * Toggle children on click.
             * @param {node} d
             */
            function click(d) {
              if (d.children) {
                d._children = d.children;
                d.children = null;
              } else {
                d.children = d._children;
                d._children = null;
              }
              update(d);
            }

            /*
             * Collapses the node d and all the children nodes of d
             * @param {node} d
            */
            function collapse(d) {
              if (d.children) {
                d._children = d.children;
                d._children.forEach(collapse);
                d.children = null;
              }
            }

            /*
             * Collapses the node in the tree
            */
            function collapseAll() {
            	root.children.forEach(collapse);
            	update(root);
            }

            /*
             * Expands the node d and all the children nodes of d
             * @param {node} d
            */
            function expand(d) {
            	if (d._children) {
            		d.children = d._children;
            		d._children = null;
            	}
            	if (d.children) {
            		d.children.forEach(expand);
            	}

            }
            /*
             * Expands all the nodes in the tree
            */
            function expandAll() {
            	root.children.forEach(expand);
            	update(root);
            }

      /*
       * dictionary of colors corresponding to the different color categories
       * defaults to a generic blue if there are no defined color categories
       * in the data set
      */
      function linkColor(linkCode) {
      	switch (linkCode)
      	{
      	  case 'Perceive':
      	  	return '#0000FF';//blue
      	    break;
      	  case 'Evaluate':
      	  	return '#FF7F00';//orange
      	  	break;
      	  case 'Predict':
      		return '#FF0000';//red
      		break;
      	  case 'Act':
          return '#0950D0';//generic blue
		  break;
      	}
      }

      function wrap(text, width) {
          text.each(function () {
              var text = d3.select(this),
                  words = text.text().split(/\s+/).reverse(),
                  word,
                  line = [],
                  lineNumber = 0,
                  lineHeight = 1.1, // ems
                  x = text.attr('x'),
                  y = text.attr('y'),
                  dy = 0, //parseFloat(text.attr('dy')),
                  tspan = text.text(null)
                      .append('tspan')
                      .attr('x', x)
                      .attr('y', y)
                      .attr('dy', dy + 'em');
              while (word = words.pop()) {
                  line.push(word);
                  tspan.text(line.join(' '));
                  if (tspan.node().getComputedTextLength() > width) {
                      line.pop();
                      tspan.text(line.join(' '));
                      line = [word];
                      tspan = text.append('tspan')
                          .attr('x', x)
                          .attr('y', y)
                          .attr('dy', lineHeight + dy + 'em')
                          .text(word);
                  }
              }
          });
      }
    d3_save_svg.embedRasterImages(svg.node());
      d3.select('#dl').on('click', function() {
        var config = {
          filename: 'ai_capabilities',
        }
        d3_save_svg.save(d3.select('svg').node(), config);
      });

  </script>

</body>



### AI Design Patterns



#### embedRasterImages(svgElement)
A convenience function for converting all referenced raster images in an SVG element to base64 data via data URI, so that it is embedded in the SVG. This ensures that the downloaded image will contain the raster image. Probably should be updated to just directly convert a referenced link to data URI instead of doing it in two separate steps.

```javascript
svg
  .append('g')
   .append('image')
      .attr('xlink:href', 'assets/test.png')
      .attr("width", 100)
      .attr("height", 100)
      .attr("x", (width / 2)  - 50)
      .attr("y", (height / 6) * 5);

d3_save_svg.embedRasterImages(svg.node());
 ```

### Contributing
`npm install` to get the development dependencies, test and build.

Testing is via [Tape](https://github.com/substack/tape) and [jsdom](https://github.com/tmpvar/jsdom). Right now the tests are pretty rudimentary. Also `index.html` serves as a good check on whether things are working.

Development is done using the [git-flow](http://nvie.com/posts/a-successful-git-branching-model/) workflow. Please merge changes into the `develop` branch.

See [CONTRIBUTING.md](/CONTRIBUTING.md) for additional information.
