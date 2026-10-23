# MVP Scope for TrueVision AI

## Objective
Build a working media analysis app that allows a user to:
- upload a media file
- analyze it
- view a result
- understand score and reasons
- view local history
- export a report
- feel safe and respected about privacy

## In Scope
- Image upload
- Video upload
- Audio upload
- Backend analysis endpoint
- Result screen
- Score / confidence / verdict
- Reasons / evidence
- Local history
- PDF export
- Privacy-safe notice
- Multi-language support (VI / EN minimum)
- Error states
- Fallback mode when model is missing

## Out of Scope
- Background microphone/camera recording
- Call monitoring
- Contact access
- Location tracking
- Real-time message scanning
- Full enterprise backend
- Advanced forensic lab features
- Commercial legal evidence claims
- Full native device integration beyond basic upload

## Must-Have UX
- User can do analysis in under 3 steps
- UI is simple and clean
- Results are readable
- Privacy message visible
- No misleading certainty language

## Must-Have Technical
- Backend runs
- API receives file and returns response
- Local history persists
- Export PDF works
- App handles invalid files
- Model fallback is clearly communicated

## Release Gate
The app is ready for a soft launch when:
- upload works
- result works
- history works
- export works
- privacy-safe wording is visible
- app does not overclaim certainty