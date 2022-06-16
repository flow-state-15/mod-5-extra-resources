# H1 Store Examples for projects

# H2 AirBnb, HipCamp, CouchSurf Store Shape:
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
```
store = {
    session: {},
    spots: {
        spotId: {
            spot data as key value pairs,
            reviews:{reviewId: {
                        reviewData,
                        user: {userData who reviewed}
                    }
            },
            images: {normalizedImageData}
        },
        optionalOrderedList: []
    }
    bookings: {
        bookingId: {
            booking data as key value pairs.
            user: {userData of user that booked}.
            spot: {spotData for the booking}
        },
        optionalOrderedList: []
    }
}
```
# H3 notes:
-when querying spot, include reviews, include images
-when the user logs in, hydrate bookings slice of state for that user
-an efficient way to add a review for example, would be to create the review in the database, json teh created review to redux, and then just add that one review to the store by repreading the old state at the upper level and the nested levels, and then adding the the new review in the normalized data


# H2 Eventbright Store Shape:
```
store = {
    session: {},
    venues: {
        venueId: {
            venue data as key value pairs,
            events: {
                eventId: {
                    event key value pairs,
                    categoryType: "category string"
                }
            }
        optionalOrderedList: []
        },
    },
    tickets: {
        ticketId: {
            ticket data as key value pairs,
            user: {userData of who booked ticket},
            event: {eventData for this event}
        },
        optionalOrderedList: []
    }
}
```
# H3 notes:
-query venue and include event, nest include category but alias as lowercase category and use attributes array to only return one column: type
-tickets is mainly related to user so makes sense to make it it's own slice of state


# H2 Evernote Store Shape:
```
store = {
    session: {},
    notebooks: {
        notebookId: {
            ticket data as key value pairs,
            notes: {normalizedNotes}
        },
        optionalOrderedList: []
    }
}
```


# H2 Flickr Store Shape:
```
store = {
    session: {},
    userAlbums: {
        albumId: {
            album data as key value pairs,
            images: { normalizedImages },
            optionalOrderedList: []
        },
    singleImage: { //optional
            image key value pair,
            comments: {
                normalizedComments,
                user: {user who left review}
            },
            optionalOrderedList: []
        },
    allImages: [array of images for the splash page potentially, or all images for a specific album]
}
```
# H3 notes:
-one slice of state for album and images
-one slice of state for a image detail page
-and an all image array for the splash page or we can even use it to hold images for an album


# H2 Medium Store Shape:
# H3 example 1
```
store = {
    session: {},
    stories: {
        storyId: {
            story data as key value pairs,
            optionalOrderedList: []
        },
    comments: {
        commentId: {comment key value pairs},
        optionalOrderedList: []
     },
    likes: {
        likeId: {like key value pairs},
        optionalOrderedList: []
        },
    userFollows: {normalizedUserData},
    followingUser: {normalizedUserData}
}
```
# H3 note:
-dispatch multiple thunks so more complicated on front end, but each reducers is more simple

# H3 example 2
```
store = {
    session: {},
    stories: {
        storyId: {story data as key value pairs,
        comments: {
                normalizedComment,
                user: {user who left comment}
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
# H3 note:
-normalized user data contains user data such as name
-dispatch one thunk but reducer is more complicated

# H2 MeetUp Store Shape:
```
store = {
    session: {},
    events: {
        eventId: {
            event data as key value pairs,
            user: {user who is hosting event},
            venues: {
                venueId: {
                    venue key value pairs,
                    groupId: "groupType string"
                }
            }
        optionalOrderedList: []
        },
    rsvps: {
        rsvpId: {rsvp data as key value pairs},
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


# H2 ProductHunt Store Shape:
```
store = {
    session: {},
    productDetail: {
        productId: {
                product data as key value pairs,
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
            product data as key value pairs,
            user: {data for user who asked product}
        },
        optionalOrderedList: []
    }
}
```


# H2 Quora Store Shape:
```
store = {
    session: {},
    questionDetail: {
        questionId: {
                question data as key value pairs,
                user: {data for user who asked question}
                answers: {
                    answerId: {
                            answerData,
                            user: {userData for who answered}
                    },
                    optionalOrderedList: []
                }
        }
    },
    allQuestions: {
        questionId: {
            question data as key value pairs,
            user: {data for user who asked question}
        },
        optionalOrderedList: []
    }
}
```


# H2 SoundCloud Store Shape:
```
store = {
    session: {},
    songDetail: {
        songId: {
                song data as key value pairs,
                user: {data for user who uploaded song},
                album: {
                    album data for this song,
                    user: {user who made or uplaoded album}
                }
                comments: {
                    commentId: {
                            commentData,
                            user: {userData for who commented}
                    },
                    optionalOrderedList: []
                }
        }
    },
    allAlbums: {
        albumId: {
            album data as key value pairs,
            user: {data for user who uploaded album}
        },
        optionalOrderedList: []
    }
}
```


# H2 Yelp Store Shape:
```
store = {
    session: {},
    businessDetail: {
        businessId: {
                business data as key value pairs,
                user: {data for user who uploaded business},
                reviews: {
                    reviewId: {
                            reviewData,
                            user: {userData for who reviewed}
                    },
                    optionalOrderedList: []
                }
        }
    },
    allBusinesses: {
        businessId: {
            business data as key value pairs,
            user: {data for user who uploaded business}
        },
        optionalOrderedList: []
    }
}
```
