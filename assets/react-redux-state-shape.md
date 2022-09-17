# Store Examples for projects

The examples below are to provide suggestions and inspiration for designing
your own redux store shapes.

**There is not only one correct way to implement your Redux store shape.**

Please feel free to deviate if it makes sense to you for your project.

**Only implement slices of state as you need it.** Most of these examples are
designed with 3+ features. Pick the parts you as you implement that feature.

## AirBnb Store Shape:

There are two examples for AirBnB, there are pros and cons to each approach.

For the "beginner" example, you have less nested state which may help avoid
certain kinds of bugs. However you will need to write more code for each of
different slices of states since they each need their own reducer.

For the "intermediate" example, the data structure is more nested. This should
mean less files, reducers and code. This is closer to the implementation you
would expect for typical projects.

### _BEGINNER_ AirBnb Store Shape:

```js
store = {
  // To keep things simple and not have nested objects/arrays we are going to
  // separate the route logic. (Refer to API Docs for more information)
  session: {},
  allSpots: {
    [spotId]: {
      spotData,
    },
    optionalOrderedList: [],
  },
  // Notice how singleSpot has more information than the allSpots slice.
  // Refer to your API Docs to find out what your response is for each route and match accordingly.
  singleSpot: {
    spotData,
    SpotImages: [imagesData],
    Owner: {
      ownerData,
    },
  },
  // This slice of state can be used for a single spot component of some sort.
  spotReviews: {
    [reviewId]: {
      reviewData,
      User: {
        userData,
      },
      ReviewImages: [imagesData],
    },
    optionalOrderedList: [],
  },
  // While this slice of state can be used for a component showing all of the user's own reviews.
  // Note the difference between the two data structures and make changes according to your API Docs.
  userReviews: {
    [reviewId]: {
      reviewData,
      User: {
        userData,
      },
      Spot: {
        spotData,
      },
      ReviewImages: [imagesData],
    },
  },
  // HINT: This may have different response structures based on a certain criteria. (Check your API Docs!)
  spotBookings: {
    [bookingId]: {
      bookingData,
    },
    optionalOrderedList: [],
  },
  userBookings: {
    [bookingId]: {
      bookingData,
      Spot: {
        spotData,
      },
    },
    optionalOrderedList: [],
  },
};
```

### _INTERMEDIATE_ AirBnb Store Shape:

```js
store = {
  session: {},
  spots: {
    // Notice there are two slices of state within spots. This is to handle your two different routes for getting a spot.
    // Refer to your API Docs to get more information.
    allSpots: {
      [spotId]: {
        spotData,
      },
      // These optional ordered lists are for you to be able to store an order in which you want your data displayed.
      // you can do this on the frontend instead of in your slice is state which is why it is optional.
      optionalOrderedList: [],
    },
    // Notice singleSpot has more data that the allSpots slice. Review your API Docs for more information.
    singleSpot: {
      spotData,
      SpotImages: [imagesData],
      Owner: {
        ownerData,
      },
    },
  },
  // Again the idea here is two have separate slices for the different data responses you receive from your routes.
  // For example, you could use each of these slices specifically for the component you are dealing with on the frontend.
  reviews: {
    // When on a single spot, use the spot slice.
    spot: {
      [reviewId]: {
        reviewData,
        User: {
          userData,
        },
        ReviewImages: [imagesData],
      },
      optionalOrderedList: [],
    },
    // When on the user's reviews, use the user slice.
    user: {
      [reviewId]: {
        reviewData,
        User: {
          userData,
        },
        Spot: {
          spotData,
        },
        ReviewImages: [imagesData],
      },
      optionalOrderedList: [],
    },
  },
  bookings: {
    user: {
      [bookingId]: {
        bookingData,
        Spot: {
          spotData,
        },
      },
      optionalOrderedList: [],
    },
    // Note here that your responses can actually be different here as well.
    // HINT: What information should you see if you own this spot? (Refer to API Docs).
    spot: {
      [bookingId]: {
        bookingData,
      },
      optionalOrderedList: [],
    },
  },
};
```

## MeetUp Store Shape:

```js
store = {
  session: {},
  groups: {
    allGroups: {
      [groupId]: {
        groupData,
      },
      optionalOrderedList: [],
    },
    singleGroup: {
      groupData,
      GroupImages: [imagesData],
      Organizer: {
        organizerData,
      },
      Venues: [venuesData],
    },
  },
  events: {
    allEvents: {
      [eventId]: {
        eventData,
        Group: {
          groupData,
        },
        Venue: {
          venueData,
        },
      },
    },
    // In this slice we have much more info about the event than in the allEvents slice.
    singleEvent: {
      eventData,
      Group: {
        groupData,
      },
      // Note that venue here will have more information than venue did in the all events slice. (Refer to your API Docs for more info)
      Venue: {
        venueData,
      },
      EventImages: [imagesData],
      // These would be extra features, not required for your first 2 CRUD features
      Members: [membersData],
      Attendees: [attendeeData],
    },
  },
};
```

## SoundCloud Store Shape:

```js
store = {
  session: {},
  songs: {
    allSongs: {
      [songId]: {
        songData,
      },
      optionalOrderedList: [],
    },
    singleSong: {
      songData,
      Artist: {
        artistData,
      },
      // Not a required feature for first 2 CRUD features
      Album: {},
    },
  },
  playlists: {
    allPlaylists: {
      [playlistId] : {
        playlistData
      },
      optionalOrderedList: [],
    },
    singlePlaylist: {
      playlistData,
      Songs : {
        songsData
      }
    }
  },
  // You will want some slice of state to keep track of the song being played
  // and to keep track of playlist/album for continuous play.
  songPlayer: {
    currentSong: { songData }
    currentPlaylist: {
      playlistData,
      Songs : {
        songsData
      }
    }
  },
};
```

<!-- The examples below are outdated and are not currently in use. -->
<!-- They are here only for future potential updates. -->

<!-- ## Eventbright Store Shape:

```js
store = {
    session: {},
    venues: {
        venueId: {
            venueData,
            events: {
                eventId: {
                    eventData,
                    user: (userData of host)
                    categoryType: "category string"
                }
            }
        optionalOrderedList: []
        },
    },
    tickets: {
        ticketId: {
            ticketData,
            user: {userData of who booked ticket},
            event: {eventData for this event}
        },
        optionalOrderedList: []
    }
}
```

### notes:

-query venue and include event, nest include category but alias as lowercase category and use attributes array to only return one column: type
-tickets is mainly related to user so makes sense to make it it's own slice of state

## Evernote Store Shape:

```js
store = {
  session: {},
  notebooks: {
    // note that evernote allows you to create notes without manually putting it in a notebook. Setup a default notebook for this.
    notebookId: {
      ...notebookData,
      notes: { ...normalizedNotes },
    },
    optionalOrderedList: [],
  },
};
```

## Flickr Store Shape:

```js
store = {
    session: {},
    userAlbums: {
        albumId: {
            albumData,
            images: {
                imageId: {
                    imageData,
                    user: {userData of whoever uploaded image}
                }
            },
            optionalOrderedList: []
        },
    singleImage: { //optional
            imageData,
            user: {userData of whoever uploaded image},
            comments: {
                normalizedComments,
                user: {user who left review}
            },
            optionalOrderedList: []
        },
    allImages: [array of images for the splash page potentially, or all images for a specific album]
}
```

### notes:

-one slice of state for album and images
-one slice of state for a image detail page
-and an all image array for the splash page or we can even use it to hold images for an album

## Medium Store Shape:

### example 1

```js
store = {
    session: {},
    stories: {
        storyId: {
            storyData,
            user: {userData of author},
            optionalOrderedList: []
        },
    comments: {
        commentId: {comment key value pairs},
        user: {userData of author},
        optionalOrderedList: []
     },
    likes: {
        likeId: {likeData},
        optionalOrderedList: []
        },
    userFollows: {normalizedUserData},
    followingUser: {normalizedUserData}
}
```

### note:

-dispatch multiple thunks so more complicated on front end, but each reducers is more simple

### example 2

```js
store = {
    session: {},
    stories: {
        storyId: {
            storyData,
            user: {userData of author},
            comments: {
                normalizedComment,
                user: {userData of author},
            },
            likes: {
                likeId: likeData,
            }
            optionalOrderedList: []
        },
    userFollows: {normalizedUserData},
    followingUser: {normalizedUserData},
}
```

### note:

-normalized user data contains user data such as name
-dispatch one thunk but reducer is more complicated

## ProductHunt Store Shape:

```js
store = {
    session: {},
    productDetail: {
        productId: {
                productData,
                user: {user who owns product},
                reviews: {
                    reviewId: {
                            reviewData,
                            user: {userData}
                    },
                    optionalOrderedList: []
                }
        }
    },
    allProducts: {
        productId: {
            productData,
            user: {userData}
        },
        optionalOrderedList: []
    }
}
```

## Quora Store Shape:

```js
store = {
    session: {},
    questionDetail: {
        questionId: {
                questionData,
                user: {userData of author}
                answers: {
                    answerId: {
                            answerData,
                            user: {userData of author}
                    },
                    optionalOrderedList: []
                }
        }
    },
    allQuestions: {
        questionId: {
            questionData,
            user: {userData of author}
        },
        optionalOrderedList: []
    }
}
```

## Yelp Store Shape:

```js
store = {
    session: {},
    businessDetail: {
        businessId: {
                businessData,
                user: {userData for business owner},
                reviews: {
                    reviewId: {
                            reviewData,
                            user: {userData of author}
                    },
                    optionalOrderedList: []
                }
        }
    },
    allBusinesses: {
        businessId: {
            businessData,
            user: {userData for business owner}
        },
        optionalOrderedList: []
    }
}
```
-->
