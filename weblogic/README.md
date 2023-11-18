This script can easily be run with:

    chown root.root /usr/local/sbin/weblogic_tmp_cleanup
    chmod 755  /usr/local/sbin/weblogic_tmp_cleanup

    cat >/etc/cron.d/weblogic_tmp_cleanup <<EOF
    0 1 * * *       root    /usr/local/sbin/weblogic_tmp_cleanup
    EOF

    service cron reload
