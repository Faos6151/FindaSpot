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
