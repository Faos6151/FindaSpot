# A/B Testing

## A/B Test Name: "Login Page User Message"

**User Story Number:** US2 (Login)

**Metrics:**
- **Happiness:** Measure user satisfaction with the login experience.
- **Task Success:** Measure the percentage of users who successfully log in.
- **Adoption:** Measure the number of users who successfully log in and begin using the application.

**Hypothesis:**

We hypothesize that changing the welcome message on the login page to be more engaging, welcoming, and informative will increase the number of successful user logins because users may be more encouraged to log in when greeted with a friendly message that clearly communicates the value of using the application.

**What problem are we trying to solve? What is its impact?**

The current login page may not provide enough encouragement or information to motivate users to log in. A generic welcome message may fail to create a positive first impression or remind users of the value of the application. This could contribute to fewer users completing the login process, ultimately reducing user engagement and adoption. Improving the welcome message could create a more inviting experience and encourage users to complete the login process.

**Experiment:**

We will use Firebase A/B Testing and Firebase Remote Config to test two different welcome messages on the login page.

- **Audience:** All users who visit the login page will be eligible for the experiment.
- **User Allocation:** Users will be randomly divided into two groups, with 50% assigned to the control group and 50% assigned to the variation group.
- **Control Group (A):** Users will see the current welcome message.
- **Variation Group (B):** Users will see the new, more engaging welcome message.
- **Duration:** The experiment will run for approximately one weeks to collect enough data to compare the results.
- **Tracking:** Firebase Analytics will track the following events:
  - `login_page_view`: Tracks when a user visits the login page.
  - `login_attempt`: Tracks when a user attempts to log in.
  - `login_success`: Tracks when a user successfully logs in.
  - `login_failure`: Tracks unsuccessful login attempts.

We will compare the login success rate between the two groups to determine whether the new welcome message improves successful logins. We will also compare login attempts and failures to better understand user behavior.

**Variations:**

**Control (A) – Current Welcome Message**

Users will see the existing login page welcome message without any changes.

**Variation (B) – Updated Welcome Message**

Users will see a more engaging and informative welcome message designed to encourage them to log in.

Example:

- **Control (A):** "Real-time availability for students and faculty across all campus zones."
- **Variation (B):** "Welcome Back! Your Next Experience Starts Here. Log In to Continue!"

Only the welcome message will change between the two variations. The login form, buttons, colors, and overall layout will remain identical to ensure that the experiment measures the impact of the welcome message alone.


## A/B Test Name 2: "Profile Tagline and Notifications".

**Metrics:**
- **Task Success:** Measure the percentage of users who complete the onboarding.
- **Adoption:** Measure the number of users who successfully complete the onboarding and continue to using the application.

**Hypothesis:**

We believe that users are more likely to complete the onboarding if the tag line "Park Easy" is shown and the notification section is removed form the onboarding flow, as it will allow less content to be shown on the page and give users an easier time to complete it. 

**What problem are we trying to solve? What is its impact?**

The set up profile page may be a bit cluttered and might not be the most motivational for users to complete. The simple tagline and direct notification button may cause some resistance for users to start using the application. This could lead to fewer users, reducing engagement for the app and adoption. 

**Experiment:**

For this experiment 50% of users will get the normal screen with the text "Personalize your experience" with the notification toggle while the other 50% will get the new screen with the tagline "Park Easy" and no notification toggle for real time spot reports, auto detect location.

- **Duration:** The experiment will run for approximately one weeks to collect enough data to compare the results.

**Variations:**

**Control (A) – Current Welcome Message**

or this experiment 50% of users will get the normal screen with the text "Personalize your experience

**Variation (B) – Updated Welcome Message**

Notification toggle while the other 50% will get the new screen with the tagline "Park Easy" and no notification toggle for real time spot reports.


## **A/B Test Name 3: “Map Layer Options: Topographical and Satellite View”**

**Metrics**

**User Story Number:** 3
Task Success: Measure the percentage of users who successfully find and use their intended map view (e.g., switch layers and then complete a navigation or location-search action within the same session).

Adoption: Measure the number of users who use the map layer feature and continue to return to the map widget in later sessions.

**Hypothesis**

We believe that users are more likely to engage with the map widget and complete location-based tasks if topographical and satellite views are offered through a clearly labeled layer control. Users can then match the map to their goal (terrain for hiking, satellite for visual landmarks) without leaving the widget, which should reduce friction and increase task completion.

What problem are we trying to solve? What is its impact?

The map widget currently offers a single default view, which may not suit every use case. Users who need elevation detail or real-world imagery may feel the map lacks the information they need, leading them to leave the app for another map provider. This could reduce time spent in the app, lower task completion, and hurt retention and adoption.

**Experiment**

For this experiment, 50% of users will see the current map widget with the standard default view only. The other 50% will see the updated widget with a layer toggle offering Default, Topographical, and Satellite views.

Duration: The experiment will run for approximately two weeks to collect enough data, including weekday and weekend usage patterns, to compare results.

**Variations**

Control (A): Current Map Widget
Users see the standard map with no option to change the view. Zoom, pan, and search behave as they do today.

Variation (B): Updated Map Widget with Layer Options
Users see the same map plus a layer button (top-right corner) that lets them switch between Default, Topographical, and Satellite views. The selected view persists for the rest of the session.
