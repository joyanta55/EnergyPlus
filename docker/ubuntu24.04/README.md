Dockerfile
-------
Create Dockerfile rules to export energyPlus. Run 

.. code-block:: console

    docker build --no-cache -t energyplus .
to build the docker image. Followed by

.. code-block:: console

    docker run energyplus -h

Please make sure to mount your python source code library with the `docker run` command. Example shown, if you want to scan your python source code located in `/tmp` directory (/tmp/buggy_python.py)

.. code-block:: console

    docker run -v /tmp:/mnt/tmp bandit /mnt/tmp/buggy_python.py
I have attched a sample buggy python code in the repo (buggy_python.py). Just cp buggy_python.py /tmp/buggy_python.py. And run the above docker command.