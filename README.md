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