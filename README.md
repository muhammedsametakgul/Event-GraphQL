# Event-User-Location-Participants GRAPHQL

## How can I use this repository?

To Start:

1. Open project with VS Code.
2. Run `npm install` .
3. Run  `npm start` .

   # SCHEMA:

```graphql
# Get All Users
query getAllUsers {
  users {
    id
    username
    email
  }
}

# Get One User
query getOneUser {
  user(id: 25) {
    id
    username
    email
  }
}

# Get All Events
query getAllEvents {
  events {
    id
    title
    desc
    date
    from
    to
    location_id
    user_id
    user {
      id
      username
      email
    }
    participants {
      id
      user_id
      event_id
    }
    location {
      id
      name
      lat
      lng
    }
  }
}

# Get One Event
query getOneEvent {
  event(id: 1) {
    title
  }
}

# Get All Participants
query getAllParticipants {
  participants {
    id
    user_id
    event_id
  }
}

# Get One Participant
query getOneParticipant {
  participant(id: 1) {
    id
    user_id
    event_id
  }
}

# Get All Locations
query getAllLocations {
  locations {
    id
    name
    desc
    lat
    lng
  }
}

# Get One Location
query getOneLocation {
  location(id: 1) {
    id
    name
    desc
    lat
    lng
  }
}




