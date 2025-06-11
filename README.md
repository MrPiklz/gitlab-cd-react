# gitlab-cd-react
This is test REP for CI/CD with react
git clone https://github.com/ntaranov/gitlab-cd-react
cd gitlab-cd-react
export NODE_OPTIONS=--openssl-legacy-provider
npm install
npm run build
npm run test -- --coverage --watchAll=false --forceExit
npm start


Next steps in local GitLab

#git push https://gitlab.com/<user name>/gitlab-cd-react
git push https://gitlab.local/root/gitlab-cd-react  #127.0.0.1//local ip

##################
Nginx Config

server {
        listen 8080;
        listen [::]:8080;
        location / {
                # First attempt to serve request as file, then
                # as directory, then fall back to displaying a 404.
                root /var/www/gitlab-cd-react/build/;
                try_files $uri $uri/ =404;
        }
}
##################