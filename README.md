# DEMO For NatGeo Microsoft AI4Earth Natural Capital Project API

NOTE: this project was designed to detect all dams globally and not necessarily at a per-image level as the API below demos. We suggest users visit https://github.com/natcap/natgeo-dams for a high performace tuned pipeline demo.

Install the Docker image:

``docker pull natcap/1.0-natgeo-dams:1 docker run --rm -it -p 8080:8080 -v pwd:/usr/local/images 1.0-natgeo-dams:1``

The API has only one entry point:
* ``api/v1/process_image``
* and takes only a content type of `image/png`
* If the API returns success the content will be a JSON object with a list of bounding boxes and scores for detect dams in pixel coordinates: ``[[[xmin0, ymin0, xmax0, ymax0], score0],  [[xmin1, ymin1, xmax1, ymax1], score1], ...]``
