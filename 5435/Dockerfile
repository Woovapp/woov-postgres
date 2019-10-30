FROM postgres:11 as orig

FROM scratch as postgres
COPY --chown=999:999 --from=orig / /
ENTRYPOINT docker-entrypoint.sh -c port=5435
EXPOSE 5435
CMD ["postgres"]