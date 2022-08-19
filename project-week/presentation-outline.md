# Presentation Format

This is an outline of the steps you will take for your presentations of the
project on Monday of W17.

## Conditions for passing

- No more commits may be pushed after 8:00am PT on day of presentations.
- All grading will be done on your live Heroku app. No exceptions.
- All students will present to their respective teams.
- Presenting work to others is an important part (if not common) of the regular
  job as a SWE. This is practice for that.
- If you would like to practice/prepare, demo with yourself, or your peers.

## Presentation Walkthrough

1. Demo splash page:

   - All links must be valid and cannot be dead. Be mindful of styling that
     looks like links. This must be intuitive. If you're not sure what's a link
     ask yourself, or your peers if something looks like a link that would
     navigate you elsewhere.

   - Instructors will ask you to click on these links during presentation.

2. Auth

   - Sign Up:

     - Showcase validation errors first.
     - Sign up successfully.
     - Log out.

   - Log In:

     - Showcase validation errors first.

     - Log in with previously made user.
     - Log out.

   - Demo user:
     - Log in with demo user button. Recall this feature is on your scorecard.

3. Feature 1:

   - Create:

     - Showcase error handling for failed cases.
     - Successfully create item (whatever it is your website does).

   - Read:

     - Previously created item should now be visible somewhere. Showcase this.

   - Update:

     - Successfully update item.

     - Showcase item being changed.

   - Delete:

     - Delete item successfully.

     - NOTE: You may want to wait to do this if your second Feature depends on
       this first feature. You may circle back to this and showcase Delete for
       both features at the same time. This will speed up your presentation
       significantly.

     - Successfully showcase item is no longer present.

     - This INCLUDES scenarios where it should cascade Delete (i.e., Delete a
       "Spot" that has "Reviews/Bookings", now those should also have been
       deleted.

4. Feature 2:

   - Repeat all steps for Feature 1, but no Update.

   - Note, you may want to create TWO items. One to showcase individual Delete.
     Another to let your Feature 1 cascade Delete (if applicable).

Following all of those steps will satisfy every part of the scorecard except
parts of General Requirements. Staff will grade these later after you
presentations.
