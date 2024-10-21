# Implementing SSO between Okta and Tableau

Scenario : As an IAM analyst, you're tasked with configuring Single Sign-On (SSO) between Okta and Tableau Cloud for a growing enterprise that uses Tableau for data analytics. The goal is to streamline access for users, improve security, and centralize authentication.




## First we login to our Okta tentant, Okta will server as our Idp, once logged in we then navigate to applications
![image](https://github.com/user-attachments/assets/60890914-765d-4bd0-a797-9e97dce78b52)


### Okta has an app catalog that gives us access to a lot of applications, click this and search Tableau Cloud
![image](https://github.com/user-attachments/assets/d00b4218-73b4-44f3-944d-032eb98439ce)



#### Click add integration, name the application and click done

From here we see that we need to add the entity ID and ACS URL. This is the information we take from the SP(Service Provider)
![image](https://github.com/user-attachments/assets/4b3f7348-321a-409d-9a0a-acd3a5603495)


#### Login into Tableau Cloud > Settings > Authentication
From here we can see the info we need to copy. Copy and paste it into Okta and save

![image](https://github.com/user-attachments/assets/f3430061-591f-41e3-bb28-1a832f2e7273)


![image](https://github.com/user-attachments/assets/871a9751-46e0-4deb-bbf1-e3ead5dd5db9)


#### Next we need to exchange our Idp Info with Tablaeu. To do this, we need to upload our metadata from Okta into Tablaeu

To do this we copy and paste the metadata link from okta into our web browser, then copy and paste it into a text editor and save it as an xml file

![image](https://github.com/user-attachments/assets/108721be-b761-4f1f-95b0-42b18a28289c)

![image](https://github.com/user-attachments/assets/76739d06-c435-482f-ab89-107a807ec9fb)


![image](https://github.com/user-attachments/assets/ac24e3e4-c598-4ba2-89fd-73443bf293e4)

## Then we upload our file to Tableau and the information automatically gets filled in

![image](https://github.com/user-attachments/assets/4bd045a1-b079-4185-a955-eab72dbcbacb)


Next we need to map attributes, by default the username attribute in okta is our user emails

![image](https://github.com/user-attachments/assets/4d267b4b-b69e-4fb2-907c-1da6ecc011d0)


Save and head back to okta

![image](https://github.com/user-attachments/assets/fa8eebf8-c11e-4840-bbbc-e1de73c7540d)



## We now need to assign a user to this application. Alex Bailey is responsible for our tableau work so it'll be assigned to him

![image](https://github.com/user-attachments/assets/af5f7c44-7b70-4b0c-be27-4d8106ee7305)


![image](https://github.com/user-attachments/assets/0418c8b8-cb07-40f8-baec-f5395d20f302)


# Next we need to create the same user in Tableau

Navigate to Tableau > Users > Then create the user
![image](https://github.com/user-attachments/assets/6f3fe3ed-2fca-4b52-888d-c25483bf0b16)


# Now time to test it
![image](https://github.com/user-attachments/assets/4aed3db1-f40b-4110-94f6-1a240038b34e)



![image](https://github.com/user-attachments/assets/6bbad9df-ceb2-46dc-9524-16def227e2bd)


![image](https://github.com/user-attachments/assets/efc6c6b5-99c4-472f-9d52-32136f7d41bc)




# Summary

This lab showcases sso between Okta and Tableau
- SAML exchanges information between the Idp and SP
- SSO allows for our user to login to many applications with one single login


