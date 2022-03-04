# Calendar Journal

This is a single page daily journaling app that uses Google Calendar as a storage backend. It's a static page, so you can host it anywhere. I host it in Google Cloud Storage.

## Installation

1. Create (or reuse) a [Google Cloud Platform project](https://developers.google.com/workspace/guides/create-project).
1. [Enable the Google Calendar API](https://console.cloud.google.com/apis/library/calendar-json.googleapis.com) on the project.
1. Create an OAuth Client ID for the project and set `CLIENT_ID` to the client ID you get from the [Google Developers Console](https://console.cloud.google.com/apis/credentials).
1. Edit the OAuth Client you just created and add the domain you want to use. This can take forever to update so it's best to do this first.
1. Create an API Key for the project and set `API_KEY` to the API Key you get from the Google Developers Console. You can restrict access of the API Key to just the Calendar API.
1. Create a Calendar in [Google Calendar](https://calendar.google.com). Make sure it has a unique name (I called mine "Journal").
1. Set `calendarName` to the name of the Calendar you created.

Once all of the changes propogate through Google, you should be able to use the app. On first load, you have to click the "Authorize" button at the top left. You will be asked to grant access to the Calendar API, your cloud project will be the name of the app. Google will warn you it's unverified, but if you trust yourself to handle your data, then go for it.

## Formatting

I'm pretty sure Google Calendar supports arbitrary HTML formatting. The WYSIWYG editor can do far more than Google Calendar can. It doesn't show up in the calendar, but it shows up in this app, so you can embed all sorts of stuff.

## Future Work

If I ever get around to it, I'd like to add the following features:

* **Attachments** - The Google Calendar API supports Google Drive attachments. So that could be neat. But the WYSIWYG editor supports embedding images via URL so... is that even necessary?
* **Tags** - I'd like to add tags to the journal entries. I'd like to be able to filter the entries by tag.
* **Colors** - I'd like to be able to set the color of the journal entry.
* **Better Mobile Layout** - I'd like the app to not suck on mobile.
* **Multiple Entries Per Day** - This app has one entry per day. Would it even be useful to have multiple entries per day?
* **Arbitrary Data** - The Calendar API supports arbitrary key-value storage. So that could be neat, but would it be useful to have a journal that could store arbitrary data? Maybe, but that can also be encoded in the journal entry itself.

## Credits

This app uses the following libraries:
 * jQuery
 * jQuery UI
 * Bootstrap
 * Moment.js
 * Summernote

## License
GPL v3