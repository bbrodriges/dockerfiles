FROM node:6

RUN npm i -g 'raml2html/raml2html'

RUN mkdir -p /app

VOLUME /app

CMD if [ -z "$TPL" ]; then raml2html -i /app/$INPUT -o /app/$OUTPUT; else raml2html -t /app/$TPL -i /app/$INPUT -o /app/$OUTPUT; fi