FROM postgres:11 as orig

FROM scratch as postgres
COPY --chown=postgres:postgres --from=orig / /
ENTRYPOINT docker-entrypoint.sh -c port=5433
EXPOSE 5433
CMD ["postgres"]