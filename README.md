[![Edit in Eraser](https://firebasestorage.googleapis.com/v0/b/second-petal-295822.appspot.com/o/images%2Fgithub%2FOpen%20in%20Eraser.svg?alt=media&token=968381c8-a7e7-472a-8ed6-4a6626da5501)](https://app.eraser.io/workspace/8RJZpgQQjbfajWeMH7Vv)
## [﻿vite](https://vitejs.dev/) + [﻿React](https://reactjs.org/) + [﻿TypeScript](https://www.typescriptlang.org/) Starter
This setup includes:

- [﻿vite](https://vitejs.dev/) 
- [﻿eslint](https://eslint.org/), [﻿typescript-eslint](https://typescript-eslint.io/), [﻿eslint-airbnb-config](https://github.com/airbnb/javascript), [﻿prettier](https://prettier.io/) 
- [﻿vitest](https://vitest.dev/), [﻿jsdom](https://github.com/jsdom/jsdom), [﻿@testing-library](https://testing-library.com/) 
- [﻿react-router v6](https://reactrouter.com/en/main)
- husky and lintstaged
- gh pages for FE deployment

# deployment info

Don't forget to update "homepage" in package.json!!

You should be able to just clone this and github actions + pages should do the rest.

However on first build you need to bootstrap:

```
npm i
npm run build
npm run deploy
```

Then go to github dashboard UI, "Settings", "Pages", and make sure it shows up.

Also need to update secrets:

upper right avatar -> settings -> developer settings -> personal access tokens

create a new token with repo-specific permissions 
```
Read access to metadata
Read and Write access to actions, administration, code, deployments, issues, merge queues, pages, pull requests, repository hooks, and workflows 
```
or reuse an existing token.

Copy the token

then go to the repo -> settings -> secrets -> actions secrets and create a new secret called "ACTIONS_DAT" and paste in the generated value.

Go to github actions and view the logs. if you see "403" permission not granted, you didn't paste it in right, or you didn't give it all the permissions (check "code" especially).


## research

https://stackoverflow.com/questions/72740796/fatal-could-not-read-password-for-https-github-com-no-such-device-or-a

Deployment setup:

Build on github pages:
https://medium.com/mobile-web-dev/how-to-build-and-deploy-a-react-app-to-github-pages-in-less-than-5-minutes-d6c4ffd30f14

https://docs.github.com/en/free-pro-team@latest/github/working-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

https://create-react-app.dev/docs/deployment/

Github actions: https://dev.to/dyarleniber/setting-up-a-ci-cd-workflow-on-github-actions-for-a-react-app-with-github-pages-and-codecov-4hnp




# Commit hooks
![On clone](/.eraser/8RJZpgQQjbfajWeMH7Vv___vr5tT4ZEODXKX3Gtw7O6a8eMIEh1___---figure---yc2OGdmsfm2iCcRx8LgPI---figure---jMY2Urgvt9wq623CGzBldQ.svg "On clone")

![While working](/.eraser/8RJZpgQQjbfajWeMH7Vv___vr5tT4ZEODXKX3Gtw7O6a8eMIEh1___---figure---qZvsIvCAFPyA_lEf9ER8b---figure---AIWF82xAuc-MyjD64zC4mw.svg "While working")

# References
- [﻿https://markus.oberlehner.net/blog/using-testing-library-jest-dom-with-vitest/](https://markus.oberlehner.net/blog/using-testing-library-jest-dom-with-vitest/) 
- [﻿https://testing-library.com/docs/queries/about#priority](https://testing-library.com/docs/queries/about#priority) 
- [﻿https://kentcdodds.com/blog/common-mistakes-with-react-testing-library](https://kentcdodds.com/blog/common-mistakes-with-react-testing-library) 
- 
- [﻿https://gist.github.com/shahsagarm/4017ae2a918d15b673299be400157062](https://gist.github.com/shahsagarm/4017ae2a918d15b673299be400157062) 
- [﻿https://gist.github.com/silver-xu/1dcceaa14c4f0253d9637d4811948437](https://gist.github.com/silver-xu/1dcceaa14c4f0253d9637d4811948437) 
- [﻿https://www.youtube.com/watch?v=cchqeWY0Nak](https://www.youtube.com/watch?v=cchqeWY0Nak) 
- [﻿https://www.phind.com/search?cache=c1fa81da-d38a-4e29-b774-f4f7b7df947e](https://www.phind.com/search?cache=c1fa81da-d38a-4e29-b774-f4f7b7df947e) 
- 

## BUGS

For hosting on ldjam.com, was getting the following issue

https://stackoverflow.com/questions/66808918/content-security-policy-meta-tag-within-sandboxed-iframe-not-working-in-safari

Refused to load <asset/*.js> because it appears in neither the script-src directive nor the default-src directive of the Content Security Policy.

Filed here: https://github.com/JammerCore/JammerCore/issues/2234

workaround: vite config to export a single fat html. https://github.com/vitejs/vite/issues/621


<!--- Eraser file: https://app.eraser.io/workspace/8RJZpgQQjbfajWeMH7Vv --->
