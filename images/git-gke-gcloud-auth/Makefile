# Copyright 2020 The Kubernetes Authors.
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

push-prod:
	../../hack/make-rules/go-run/arbitrary.sh run ./images/builder --project=k8s-prow --scratch-bucket=gs://k8s-testimages-scratch images/git-gke-gcloud-auth

push:
	../../hack/make-rules/go-run/arbitrary.sh run ./images/builder --allow-dirty images/git-gke-gcloud-auth

.PHONY: push push-prod
