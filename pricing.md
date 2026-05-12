{
  "$schema": "https://json-schema.org/draft/2020-12/schema",
  "title": "RepositoryImprovementIntake",
  "type": "object",
  "additionalProperties": false,
  "required": [
    "repo_url",
    "owner_authorization_confirmation",
    "access_type",
    "requested_goal",
    "allowed_scope",
    "disallowed_actions",
    "preferred_output",
    "commercial_context",
    "risk_level",
    "notes"
  ],
  "properties": {
    "repo_url": {
      "type": "string",
      "format": "uri"
    },
    "owner_authorization_confirmation": {
      "type": "object",
      "additionalProperties": false,
      "required": [
        "confirmed",
        "confirmed_by",
        "relationship_to_repo",
        "confirmation_date"
      ],
      "properties": {
        "confirmed": {
          "type": "boolean",
          "const": true
        },
        "confirmed_by": {
          "type": "string",
          "minLength": 2
        },
        "relationship_to_repo": {
          "type": "string",
          "enum": [
            "owner",
            "maintainer",
            "employee",
            "contractor_with_permission",
            "client_representative"
          ]
        },
        "confirmation_date": {
          "type": "string",
          "format": "date"
        }
      }
    },
    "access_type": {
      "type": "string",
      "enum": [
        "public_open_source",
        "private_owner_granted",
        "client_owned"
      ]
    },
    "requested_goal": {
      "type": "string",
      "minLength": 10
    },
    "allowed_scope": {
      "type": "array",
      "items": {
        "type": "string",
        "enum": [
          "static_code_review",
          "dependency_review",
          "configuration_review",
          "test_quality_review",
          "ci_cd_review",
          "documentation_review",
          "small_safe_fixes",
          "minimal_pull_request",
          "github_issue_pr_summary",
          "client_facing_report"
        ]
      },
      "minItems": 1,
      "uniqueItems": true
    },
    "disallowed_actions": {
      "type": "array",
      "items": {
        "type": "string"
      },
      "default": [
        "live_system_testing",
        "credential_use",
        "exploitation",
        "automated_vulnerability_scanning",
        "bypassing_protections",
        "third_party_infrastructure_testing"
      ]
    },
    "preferred_output": {
      "type": "object",
      "additionalProperties": false,
      "required": [
        "language",
        "format",
        "include_pr"
      ],
      "properties": {
        "language": {
          "type": "string",
          "enum": [
            "en",
            "es",
            "both"
          ]
        },
        "format": {
          "type": "string",
          "enum": [
            "markdown",
            "pdf",
            "github_issue",
            "pull_request_description"
          ]
        },
        "include_pr": {
          "type": "boolean"
        }
      }
    },
    "commercial_context": {
      "type": "object",
      "additionalProperties": false,
      "required": [
        "business_type",
        "primary_users",
        "revenue_critical",
        "deadline"
      ],
      "properties": {
        "business_type": {
          "type": "string"
        },
        "primary_users": {
          "type": "string"
        },
        "revenue_critical": {
          "type": "boolean"
        },
        "deadline": {
          "type": [
            "string",
            "null"
          ],
          "format": "date"
        }
      }
    },
    "risk_level": {
      "type": "string",
      "enum": [
        "low",
        "medium",
        "high"
      ]
    },
    "notes": {
      "type": "string"
    }
  }
}
