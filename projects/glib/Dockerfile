# Copyright 2018 Google Inc.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#      http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
#
################################################################################

FROM gcr.io/oss-fuzz-base/base-builder
MAINTAINER pdknsk@gmail.com
RUN apt-get update && \
    apt-get install -y autoconf libtool ninja-build python3-pip
RUN pip3 install -U meson
RUN git clone https://gitlab.gnome.org/GNOME/glib
WORKDIR glib
COPY build.sh fuzz.options fuzz_bookmark.c fuzz_markup.c fuzz_key.c $SRC/
