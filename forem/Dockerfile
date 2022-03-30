FROM quay.io/headline_design/forum-2

# We create the localimages/uploads symlink to enable serving images from 
# the Rails server in production. 
# See https://github.com/forem/forem/issues/13307 for more details.
RUN mkdir /opt/apps/forem/public/localimages

ADD ./scripts scripts/
ADD ./app app/
