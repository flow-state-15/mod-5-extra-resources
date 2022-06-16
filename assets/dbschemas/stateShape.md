# Store Examples for projects

## AirBnb, HipCamp, CouchSurf Store Shape:
<!-- store = {
    session: {},
    spots: {
        ...normalizedData, optionalOrderedList: []
        },
    reviewsForOneSpot: {
        ...normalizedData, optionalOrderedList: []
        },
    bookings: {
        ...normalizedData, optionalOrderedList: []
        },
    images: {
        ...normalizedData, optionalOrderedList: []
        }
} -->
```js
store = {
    session: {},
    spots: {
        spotId: {
            spotData,
            reviews:{
                reviewId: {
                        reviewData,
                        user: {userData for who reviewed}
                    }
            },
            images: {normalizedImageData}
        },
        optionalOrderedList: []
    }
    bookings: {
        bookingId: {
            bookingData,
            user: {userData of user that booked}.
            spot: {spotData for the booking}
        },
        optionalOrderedList: []
    }
}
```
### notes:
-when querying spot, include reviews, include images
-when the user logs in, hydrate bookings slice of state for that user
-an efficient way to add a review for example, would be to create the review in the database, json teh created review to redux, and then just add that one review to the store by repreading the old state at the upper level and the nested levels, and then adding the the new review in the normalized data


## Eventbright Store Shape:
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
        notebookId: {
            ticketData,
            notes: {normalizedNotes}
        },
        optionalOrderedList: []
    }
}
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

## MeetUp Store Shape:
```js
store = {
    session: {},
    events: {
        eventId: {
            eventData,
            groupId: "groupType string", //this is categoryId in the db schema image
            user: {user who is hosting event},
            venue: {
                venueData
            }
        optionalOrderedList: []
        },
    rsvps: {
        rsvpId: {
            rsvpData,
            user: {userData},
            event: {eventData}
        },
        optionalOrderedList: []
        },
    groups: {
        normalizedGroupData,
        users: {normalizedUserData},
        events: {normalizedEventData},
        optionalOrderedList: []
        }
}
```


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


## SoundCloud Store Shape:
```js
store = {
    session: {},
    songDetail: {
        songId: {
                songData,
                user: {userData of author},
                album: {
                    albumData,
                    user: {userData of author}
                }
                comments: {
                    commentId: {
                            commentData,
                            user: {userData of author}
                    },
                    optionalOrderedList: []
                }
        }
    },
    allAlbums: {
        albumId: {
            albumData,
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
