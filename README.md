# React Firebase Chat App

This project utilizes React and Firebase to create a chat application.    

*Compny*: CODTECH IT SOLUTIONS    
*NAME*: Annu Priya      
*INTERN ID*: CT08RKN       
*DOMAIN*: FRONTED END DEVELOPER       
*DURATION*: 4 WEEKS      
## CODE DESCRIPTION OR WEBSITE  
![Image](https://github.com/user-attachments/assets/1d0c12e2-79f0-4a46-8d5d-1b4bd64a201d)

![Image](https://github.com/user-attachments/assets/30b772b9-3b23-4c8d-b63b-9c5d478fa40e)

![Image](https://github.com/user-attachments/assets/3cf3b489-dfb0-4ac1-a3ee-ed0ed0c80302)

![Image](https://github.com/user-attachments/assets/879010e5-e08f-49cf-9e45-9e12461e59c2)

## Getting Started      

Follow these steps to set up and run the project locally:

### Prerequisites

- Node.js and npm installed on your machine.
- Firebase account.

### Installation

1. Clone the repository:

```bash
git clone <repository_url>
```

2. Navigate to the project directory:

```bash
cd react-firebase-project
```

3. Install dependencies:

```bash
npm install
```

### Development

1. Start the development server:

```bash
npm run dev
```

2. Open your browser and go to http://localhost:<port>

## Firebase Setup

Follow these steps to configure Firebase services for the project:

1. Create a Firebase project on the [Firebase Console](https://console.firebase.google.com/).

2. Enable Firebase Authentication and configure Google and Email/Password as Sign-In Providers.

3. Enable Firebase Cloud Firestore.

4. Add the following Firestore Security Rules:

```firebase
rules_version = '2';

service cloud.firestore {
  match /databases/{database}/documents {
    match /{document=**} {
      allow read, write: if request.auth != null;
    }
  }
}
```

5. Add the following Firestore Indexes: `chat_messagechatRoomId Ascending timestamp Ascending __name__ Ascending`.

6. Enable Firebase Cloud Storage.

7. Add the following Cloud Storage Security Rules:

```firebase
rules_version = '2';

service firebase.storage {
  match /b/{bucket}/o {
    match /{allPaths=**} {
      allow read, write: if request.auth != null;
    }
  }
}
```

8. Copy the Firebase config keys and paste them into \`src/configs/firebase.js\` in your React project.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
