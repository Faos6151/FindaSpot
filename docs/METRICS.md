Initial Metrics: 

-NPS / User Satisfaction: Increments a loginCount field in the user's Firebase collection upon each   authentication event; when loginCount == 5 and hasCompletedNPS == false, displays the survey modal in FindaSpot and writes the score to the user's Firebase record upon submission.

Onboarding Completion Rate: This will track onboardingStarted and onboardingCompleted fields in the user's Firebase collection. It records timestamps for onboarding initiation and completion, then calculates the completion rate as the percentage of user who successfully finish onboarding out of those who started. OCR = (totalCompletedOnboarding/createdAccount)*100

CTR/ Click through rate: This will track how many times the map page is loaded and compare it to the amount of interaction with the maps markers is done. This will give us a click through rate formula of CTR = (TotalInteractionMarkers/TotalLoadsofMapPage)*100. This score is computed in a cloud function through firebase CLI and is stored inside of the firebase metrics document.
