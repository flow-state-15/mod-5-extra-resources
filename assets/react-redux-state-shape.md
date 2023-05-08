# Store Examples for projects

The examples below are to provide suggestions and inspiration for designing
your own redux store shapes.

**There is not only one correct way to implement your Redux store shape.**

Please feel free to deviate if it makes sense to you for your project.

**Only implement slices of state as you need it.** Most of these examples are
designed with 3+ features. Pick the parts you as you implement that feature.

## AirBnb Store Shape:

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