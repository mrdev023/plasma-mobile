# SPDX-FileCopyrightText: 2017 Marco Martin <mart@kde.org>
# SPDX-FileCopyrightText: 2021 Aleix Pol <apol@kde.org>
# SPDX-FileCopyrightText: 2020-2021 Nicolas Fella <nicolas.fella@kde.org>
# SPDX-FileCopyrightText: 2022 Alexey Andreyev <aa13q@ya.ru>
# SPDX-License-Identifier: GPL-2.0-or-later

plasma_add_applet(org.kde.plasma.mobile.panel
    QML_SOURCES
        qml/main.qml
        qml/LockscreenOverlay.qml
        qml/StatusBarWrapper.qml
        qml/StatusPanel.qml
    CPP_SOURCES
        phonepanel.cpp
)

target_link_libraries(org.kde.plasma.mobile.panel PRIVATE
                      Qt::Gui
                      Qt::DBus
                      Plasma::Plasma
                      KF6::I18n
                      KF6::Service
                      KF6::WindowSystem
                     )
