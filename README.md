package api

import (
        "github.com/gin-gonic/gin"
        "github.com/layer-devops/livechat-example/services/api/pkg/api/ws"
)

func AddRoutes(group *gin.RouterGroup) {
        apiGroup := group.Group("/api")
        apiGroup.GET("/ws", ws.NewForContext)
        AddLoginRoutes(apiGroup)
}# Full-stack livechat example

This repository contains a [slack](https://slack.com) clone made with [PostgreSQL](https://www.postgresql.org/), [Go](https://golang.org/), and [Docker Compose](https://docs.docker.com/compose/install/)
