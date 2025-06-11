# gitlab-cd-react
This is test REP for CI/CD with react<br />
git clone https://github.com/ntaranov/gitlab-cd-react<br />
cd gitlab-cd-react<br />
export NODE_OPTIONS=--openssl-legacy-provider<br />
npm install<br />
npm run build<br />
npm run test -- --coverage --watchAll=false --forceExit<br />
npm start<br />
<br />
<br />
Next steps in local GitLab<br />
<br />
#git push https://gitlab.com/<user name>/gitlab-cd-react<br />
git push https://gitlab.local/root/gitlab-cd-react  #127.0.0.1//local ip<br />
<br />
##################<br />
Nginx Config<br />
<br />
server {<br />
        listen 8080;<br />
        listen [::]:8080;<br />
        location / {<br />
                # First attempt to serve request as file, then<br />
                # as directory, then fall back to displaying a 404.<br />
                root /var/www/gitlab-cd-react/build/;<br />
                try_files $uri $uri/ =404;<br />
        }<br />
}<br />
##################
##################
