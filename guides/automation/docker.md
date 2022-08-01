<p><a href="/">home</a> / <a href="/guides">guides</a></p>
<div class="rainbow-retro"></div>

# Containerize your Application With Docker

```yaml
FROM node:14-alpine

# install git creating working directory
RUN apk update && apk upgrade && \
    apk add --no-cache bash git openssh && \
    mkdir -p /usr/src/app

# copy files to working directory
COPY . /usr/src/app/

# change to working directory
WORKDIR /usr/src/app

# install node dependencies
RUN npm install

# expose server port
EXPOSE 3000-5001

# launch application
CMD ["npm","start"]

```
[From my Docker Repo](https://github.com/BeauBouchard/Dockerfiles/tree/main/generic/node14)

### Read More!

 * <a href="">Read more about docker</a>

<p class="spacers"> <br /></p>
<div align="center" >
  <p>
    <a href="https://beau.sh/guides/">⬅️ Back to Guides</a>
  </p>
</div>
