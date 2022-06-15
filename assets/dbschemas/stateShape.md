AirBnb, HipCamp, CouchSurf State Shape:
<!-- store = {
    session: {},
    spots: {
        ...normalizedData, list: []
        },
    reviewsForOneSpot: {
        ...normalizedData, list: []
        },
    bookings: {
        ...normalizedData, list: []
        },
    images: {
        ...normalizedData, list: []
        }
} -->
store = {
    session: {},
    spots: {
        spotId: {spot data as key value pairs, reviews:{}, images: {}}, optionalOrderedList: []
        }
    bookings: {
        bookingId: {booking data as key value pairs, reviews:{}, images: {}}, optionalOrderedList: []
        }
}
notes:
-when querying spot, include reviews, include images
-when the user logs in, hydrate bookings slive of stat for that user
-an efficient way to add a review for example, would be to create the review in the database, json teh created review to redux, and then just add that one review to the store by repreading the old state at the upper level and the nested levels, and then adding the the new review in the normalized data


Eventbright State Shape:
store = {
    session: {},
    album: {
        ...normalizedData, list: []
        },
    comments: {
        ...normalizedData, list: []
        },
    songs: {
        ...normalizedData, list: []
        }
}


Evernote State Shape:
store = {
    session: {},
    album: {
        ...normalizedData, list: []
        },
    comments: {
        ...normalizedData, list: []
        },
    songs: {
        ...normalizedData, list: []
        }
}


Flickr State Shape:
store = {
    session: {},
    album: {
        ...normalizedData, list: []
        },
    comments: {
        ...normalizedData, list: []
        },
    songs: {
        ...normalizedData, list: []
        }
}


Medium State Shape:
store = {
    session: {},
    album: {
        ...normalizedData, list: []
        },
    comments: {
        ...normalizedData, list: []
        },
    songs: {
        ...normalizedData, list: []
        }
}


MeetUp State Shape:
store = {
    session: {},
    album: {
        ...normalizedData, list: []
        },
    comments: {
        ...normalizedData, list: []
        },
    songs: {
        ...normalizedData, list: []
        }
}


ProductHunt State Shape:
store = {
    session: {},
    album: {
        ...normalizedData, list: []
        },
    comments: {
        ...normalizedData, list: []
        },
    songs: {
        ...normalizedData, list: []
        }
}


Quora State Shape:
store = {
    session: {},
    album: {
        ...normalizedData, list: []
        },
    comments: {
        ...normalizedData, list: []
        },
    songs: {
        ...normalizedData, list: []
        }
}


SoundCloud State Shape:
store = {
    session: {},
    album: {
        ...normalizedData, list: []
        },
    comments: {
        ...normalizedData, list: []
        },
    songs: {
        ...normalizedData, list: []
        }
}
