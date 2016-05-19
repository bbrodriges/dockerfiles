FROM node:6

RUN npm i -g 'raml2html/raml2md'

RUN mkdir -p /app

VOLUME /app

CMD if [ -z "$TPL" ]; then raml2md -i /app/$INPUT -o /app/$OUTPUT; else raml2md -t /app/$TPL -i /app/$INPUT -o /app/$OUTPUT; fi