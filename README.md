# new111

'''
apiVersion: networking.k8s.io/v1
kind: Ingress
metadata:
  name: nginx-ingress
  annotations:
    nginx.ingress.kubernetes.io/use-regex: "true"
spec:
  ingressClassName: nginx
  tls:
  - hosts:
    - alan-for-tf.techolution.com
    secretName: alan-for-tf.techolution.com
  rules:
  - host: "alan-for-tf.techolution.com"
    http:
      paths:
          - path: /
            pathType: ImplementationSpecific
            backend:
              service:
                name: hvpd-frontend
                port: 
                  number: 4200
     '''
