Store Examples for projects

AirBnb, HipCamp, CouchSurf Store Shape:
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
store = {
    session: {},
    spots: {
        spotId: {spot data as key value pairs, reviews:{}, images: {}}, optionalOrderedList: []
        }
    bookings: {
        bookingId: {booking data as key value pairs}, optionalOrderedList: []
        }
}
notes:
-when querying spot, include reviews, include images
-when the user logs in, hydrate bookings slice of state for that user
-an efficient way to add a review for example, would be to create the review in the database, json teh created review to redux, and then just add that one review to the store by repreading the old state at the upper level and the nested levels, and then adding the the new review in the normalized data


Eventbright Store Shape:
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
    tickets: {
        ticketId: {ticket data as key value pairs}, optionalOrderedList: []
        }
}
notes:
-query venue and include event, nest include category but alias as lowercase category and use attributes array to only return one column: type
-tickets is mainly related to user so makes sense to make it it's own slice of state


Evernote Store Shape:
store = {
    session: {},
    notebooks: {
        notebookId: {ticket data as key value pairs, notes: {normalizedNotes}}, optionalOrderedList: []
        }
}


Flickr Store Shape:
store = {
    session: {},
    userAlbums: {
        albumId: {album data as key value pairs, images: { normalizedImages}}, optionalOrderedList: []
        },
    singleImage: { //optional
        image key value pair, comments: {normalizedComments} optionalOrderedList: []
        },
    allImages: [array of images for the splash page potentially, or all images for a specific album]
}
notes:
-one slice of state for album and images
-one slice of state for a image detail page
-and an all image array for the splash page or we can even use it to hold images for an album


Medium Store Shape:
example 1
store = {
    session: {},
    stories: {
        storyId: {story data as key value pairs,
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
note:
-dispatch multiple thunks so more complicated on front end, but each reducers is more simple

example 2
store = {
    session: {},
    stories: {
        storyId: {story data as key value pairs,
        comments: {
            normalizedComment
            },
        likes: {likeId: normalizedLike, optionalOrderedList: []}
        optionalOrderedList: []
        },
    userFollows: {normalizedUserData},
    followingUser: {normalizedUserData},
}
note:
-normalized user data contains user data such as name
-dispatch one thunk but reducer is more complicated

MeetUp Store Shape:
store = {
    session: {},
    eventss: {
        eventsId: {
            events data as key value pairs,
            venues: {
                venueId: {
                    venue key value pairs,
                    groupId: "groupType string"
                }
            }
        optionalOrderedList: []
        },
    rsvps: {
        rsvpId: {rsvp data as key value pairs}, optionalOrderedList: []
        },
    groups: {
        normalizedGroupData,
        users: {normalizedUserData},
        events: {normalizedEventData}
        }

}


ProductHunt Store Shape:
store = {
    session: {},
    album: {
        ...normalizedData, optionalOrderedList: []
        },
    comments: {
        ...normalizedData, optionalOrderedList: []
        },
    songs: {
        ...normalizedData, optionalOrderedList: []
        }
}


Quora Store Shape:
store = {
    session: {},
    album: {
        ...normalizedData, optionalOrderedList: []
        },
    comments: {
        ...normalizedData, optionalOrderedList: []
        },
    songs: {
        ...normalizedData, optionalOrderedList: []
        }
}


SoundCloud Store Shape:
store = {
    session: {},
    album: {
        ...normalizedData, optionalOrderedList: []
        },
    comments: {
        ...normalizedData, optionalOrderedList: []
        },
    songs: {
        ...normalizedData, optionalOrderedList: []
        }
}
