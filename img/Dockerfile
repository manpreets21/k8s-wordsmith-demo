FROM nginx:1-alpine
RUN apk add --no-cache ca-certificates && update-ca-certificates
ADD https://get.aquasec.com/microscanner .
RUN chmod +x microscanner
RUN ./microscanner NWVjODc1ODRhYTdm
