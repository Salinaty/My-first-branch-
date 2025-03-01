# My-first-branch
branch.json
{
  "id": 3905444,
  "name": "My-first-branch",
  "target": "branch",
  "source_type": "Repository",
  "source": "Salinaty/skills-introduction-to-github",
  "enforcement": "active",
  "conditions": {
    "ref_name": {
      "exclude": [],
      "include": [
        "~DEFAULT_BRANCH"
      ]
    }
  },
  "rules": [
    {
      "type": "deletion"
    },
    {
      "type": "creation"
    },
    {
      "type": "update"
    },
    {
      "type": "required_linear_history"
    },
    {
      "type": "required_signatures"
    },
    {
      "type": "pull_request",
      "parameters": {
        "required_approving_review_count": 1,
        "dismiss_stale_reviews_on_push": false,
        "require_code_owner_review": true,
        "require_last_push_approval": true,
        "required_review_thread_resolution": true,
        "allowed_merge_methods": [
          "merge",
          "squash",
          "rebase"
        ]
      }
    },
    {
      "type": "code_scanning",
      "parameters": {
        "code_scanning_tools": [
          {
            "tool": "CodeQL",
            "security_alerts_threshold": "high_or_higher",
            "alerts_threshold": "errors"
          }
        ]
      }
    }
  ],
  "bypass_actors": [
    {
      "actor_id": null,
      "actor_type": "DeployKey",
      "bypass_mode": "always"
    },
    {
      "actor_id": 2,
      "actor_type": "RepositoryRole",
      "bypass_mode": "always"
    },
    {
      "actor_id": 4,
      "actor_type": "RepositoryRole",
      "bypass_mode": "always"
    },
    {
      "actor_id": 5,
      "actor_type": "RepositoryRole",
      "bypass_mode": "always"
    },
    {
      "actor_id": 29110,
      "actor_type": "Integration",
      "bypass_mode": "always"
    }
  ]
