FROM quay.io/forem/forem:production

# We create the localimages/uploads symlink to enable serving images from 
# the Rails server in production. 
# See https://github.com/forem/forem/issues/13307 for more details.
RUN mkdir /opt/apps/forem/public/localimages
RUN mkdir -p "${APP_HOME}"/public/{assets,images,packs,podcasts,uploads}
RUN ln -s /opt/apps/forem/public/uploads/ /opt/apps/forem/public/localimages/uploads

ADD ./scripts scripts/
ADD ./app app/
