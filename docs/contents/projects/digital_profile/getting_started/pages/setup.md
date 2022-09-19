## Digital Profile
### Initial setup
1. Pull kobo-docker and kobo-install from dolpotech organization in github
   ```
     https://github.com/dolpotech/kobo-install
     https://github.com/dolpotech/kobo-docker
     https://github.com/dolpotech/digitalprofile.git
   ```
2. First run **`make setup`** to setup up the project for first time.
3. Go to hosts.txt files  
   
        `nano  /etc/hosts`
   
4. Add these lines
   
       First obtain ip given by router to your device from ifconfig command IP is found in format `inet **.**.**.** netmask`
       
        ```
        **you-ip-address-from-router**  kf.kobo.local kc.kobo.local ee.kobo.local digital.kobo.local
        ```

       **Final /etc/hosts file setup** 
    
        ````
        ### (BEGIN) KoBoToolbox local routes
        `192.168.0.10  kf.kobo.local kc.kobo.local ee.kobo.local digital.kobo.local`
        
        `digital.kobo.local and others also cannot be changed `
        ### (END) KoBoToolbox local routes
        ````
5. Now Use Database Backup [refrence](../usage/)
5. Now Use Media Backup (optional) [refrence](../usage/)

## 
A default Digital Profile project resides in `root` directory. So, when you start the project, you will see the following screen in:

http://digital.kobo.local/
or 
http://digital.kobo.local:port_number/




##Points to remember:
1. Regularly Pull from master
   

    `git pull origin master`

   
2. Create a new branch feature/feature_name using
   

	`git checkout -b “feature/feature_name”`
   
   
3. Always pull from the master branch while starting to code. In case you forget to pull, there won’t be any issue if files conflict. In case there is merge conflict, resolve the merge conflict.
   

4. Always stay in the branch you have created to carry out task(s) and never commit to master unless asked for.
   

5. After finishing a task, commit it and push it in the branch you have created and create a pull request in GitHub.


