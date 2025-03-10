# Summary

* [Related EPIC](#related-epic)
* [Definition](#definition)
* [UI Design](#ui-design)
* [Misc](#misc)

## Related EPIC

* [Guests](./README.md)

## Definition

#### Preconditions

- Given that I am a LinShare user and I logged-in LinShare successfully

#### Description

- From menu, I go to Contacts => Guests
- I can see all guests in my domain
- When I click on three-dot button of a guest that I have simple moderator right, I can see option "Ask for admin moderator right"
- When I click on this option, then "My request" tab will be opened.
- I can see a text message: "You can send a request to become admin moderator of this guest. An admin moderator can delete guest account and manage moderator request list of that guest." and a button "Send request"
- I click on this button, there will be a popup:"You are about to send a request to become an admin moderator of this guest. Once sent, you can see the request's status in Detail panel of guest" with 2 buttons Cancel and Send
- I select "Send", then the request will be sent.
- There will be a toast message when the request was sent successfully
- After sending the request, If I am click option "Ask for admin moderator right" of that guest again, I am navigated to Details tab of that guest
- Now in Details tab, I can see a text message:" You have sent a request to become admin moderator of this guest. Please wait for approval." and a close icon

#### Postconditions

- When a request is sent, the admin moderator can see this request in the pending request list of this guest
- When I open Detail panel of the guest, I can see the text: You have sent a request to become a admin moderator of this guest" with creation date and current status of request:
  - If the request is sent successfully, it has status "Pending"
  - If the domain admin or admin moderator add me manually as moderator, this request will have status "Aborted"
  - If the request is rejected, It will have status:"Rejected"
  - If the request is approved, it will have status:"Approved"
  - When I click on Status link, it opened Activities tab of the guest.

[Back to Summary](#summary)

## UI Design

#### Mockups

![story486](./mockups/487.1.png)
![story486](./mockups/487.2.png)
![story486](./mockups/487.3.png)
![story486](./mockups/487.4.png)
![story486](./mockups/487.5.png)

#### Final design

[Back to Summary](#summary)
## Misc

[Back to Summary](#summary)