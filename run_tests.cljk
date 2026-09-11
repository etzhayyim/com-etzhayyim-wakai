(require '[clojure.test :as t])

(doseq [ns-sym '[wakai.methods.test-charter-gates
                  wakai.methods.test-pool
                  wakai.murakumo-test
                  wakai.repository-contract-test]]
  (require ns-sym))

(let [result (apply t/run-tests
                    '[wakai.methods.test-charter-gates
                      wakai.methods.test-pool
                      wakai.murakumo-test
                      wakai.repository-contract-test])]
  (System/exit (if (zero? (+ (:fail result) (:error result))) 0 1)))
