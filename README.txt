SETUP
1. Create a Firebase project on the Spark/no-cost plan.
2. Register a Web app and paste its config into firebase-config.js.
3. Enable Authentication > Email/Password.
4. Create Cloud Firestore.
5. Publish firestore.rules.
6. Create users in Firebase Authentication, then create users/{UID} in Firestore:
   {name:'Admin Name', role:'admin'}
   {name:'Employee Name', role:'employee'}
7. Open login.html.

SECURITY
Employees can CREATE daily_agenda documents but Firestore rules deny them READ/UPDATE/DELETE. Admins have full access. Do not weaken the rules.

LOGIN
This uses Firebase Email/Password authentication. Firebase's built-in password provider is email + password. A true username + password field can be added with a backend mapping, but should not be implemented as an exposed unauthenticated username directory.
