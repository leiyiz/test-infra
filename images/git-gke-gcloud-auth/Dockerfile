# Copyright 2022 The Kubernetes Authors.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

FROM google/cloud-sdk:410.0.0-alpine

ARG IMAGE_ARG
ENV IMAGE=${IMAGE_ARG}

RUN apk add --no-cache git git-daemon openssh

COPY github-known-hosts /github_known_hosts
COPY ssh-config /etc/ssh/ssh_config

RUN gcloud components install gke-gcloud-auth-plugin