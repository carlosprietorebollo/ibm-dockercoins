FROM node:4-slim
RUN npm install redis && npm install express
COPY files files
COPY webui.js .
 
FROM scratch
COPY --from=0 / /

CMD ["webui.js"]
ENTRYPOINT ["node"]
EXPOSE 8080
