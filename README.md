# Impledge_Automationfile
Three activities that are entirely focused on automation can be found in this repository: Postman Collections, SQL Queries, and Automation Source Code.
{
	"info": {
		"_postman_id": "2acfee95-8dc9-4485-8d6c-16f2391e0d76",
		"name": "Impledge_QA_Exercise",
		"schema": "https://schema.getpostman.com/json/collection/v2.1.0/collection.json",
		"_exporter_id": "8281301"
	},
	"item": [
		{
			"name": "Address - Verify",
			"event": [
				{
					"listen": "test",
					"script": {
						"exec": [
							"pm.test(\"Response body has no errors\", function () {\r",
							"    pm.expect(pm.response.text()).to.include(\"\\\"errors\\\":[]\");\r",
							"});\r",
							"\r",
							"pm.test(\"Response ZIP verified\", function () {\r",
							"    pm.expect(pm.response.text()).to.include(\"06810\");\r",
							"});\r",
							""
						],
						"type": "text/javascript"
					}
				}
			],
			"request": {
				"method": "POST",
				"header": [
					{
						"key": "Authorization",
						"value": "jBucTRfsQP5eAweqv7JQrA",
						"disabled": true
					},
					{
						"key": "Content-Type",
						"value": "application/json"
					}
				],
				"body": {
					"mode": "raw",
					"raw": " {\r\n    \"company\": \"Residence Inn\",\r\n    \"street1\": \"22 Segar St\",\r\n    \"street2\": \"\",\r\n    \"city\": \"Danbury\",\r\n    \"country\": \"US\",\r\n    \"phone\": \"855-782-3877\",\r\n    \"email\": \"shipper@mailinator.com\"\r\n  }"
				},
				"url": {
					"raw": "https://api.easypost.com/v2/addresses?verify_strict[]=delivery",
					"protocol": "https",
					"host": [
						"api",
						"easypost",
						"com"
					],
					"path": [
						"v2",
						"addresses"
					],
					"query": [
						{
							"key": "verify_strict[]",
							"value": "delivery"
						}
					]
				}
			},
			"response": []
		}
	],
	"auth": {
		"type": "basic",
		"basic": [
			{
				"key": "username",
				"value": "EZTK0126bfcd0c834208b2289e3c501630d7IMAAxVrGZ2G1UXCmomm4Pw",
				"type": "string"
			}
		]
	},
	"event": [
		{
			"listen": "prerequest",
			"script": {
				"type": "text/javascript",
				"exec": [
					""
				]
			}
		},
		{
			"listen": "test",
			"script": {
				"type": "text/javascript",
				"exec": [
					""
				]
			}
		}
	]
}
